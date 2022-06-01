# top-

## 명령어 특징
 
1. 시스템 전반을 빠르게 파악이 가능하다.
2. 옵션 없이 검색하면 interval 간격(기본 3초)으로 화면을 갱신하여 정보를 보여준다.
3. top 실행 옵션
+ 순간의 옵션을 확인하기 위해서는 -b 옵션을 추가하여 branch모드로 바꾼다.
+ -n: top의 실행 주기, 즉 반복 횟수를 지정한다.
+ top -b -n 1 : 옵션을 한번만 확인하는 코드이다.

## top 실행후 명령어 
|명령어|명령어 기능|
|:---:|:---:|
|shift + p| CPU 사용률 내림차순 |
|shift + m| 메모리 사용률 내림차순 |
|shift + t| 프로세스가 돌아가고 있는 시간순|
| k | kill.k 입력 후  PID번호 작성, signal은 9 |
| f | sort field 선택화면, q누를면 RES순으로 정렬 |
| a | 메모리 사용양에 따라 정렬 |
| b | batch 모드 작동 |
| 1 | CPU Core 사용량을 보여줌 |

## top 명령어 실행 결과 화면 
![스크린샷(25)](https://user-images.githubusercontent.com/50985536/171391560-3289987d-a499-4605-b588-2b5fd2ecfd5d.png)

|:---:|:---:|
| 19:23:02 up 2min | 7시 23분 2초에 서버가 켜졌으며 2분이 지났다. |
| load averge | 현재 시스탬이 얼마나 일을 하는자를 보여준다. 3개의 숫자는 5,10,15분간의 평균/대기 프로세스 |
| Tasks | 프로세스 개수 |
| KiB Mem, Swap | 각 메모리의 사용량 |
| PR | 실행 우선순위 |
| VIRT, RES, SHR | 메모리 사용량,누수 check 가능 |
| S | 프로세스 상태(작업중, I/O 대기, 유휴 상태 등) |

### top 명령어 실행시 나타나는 메모리 설명

+ 아래의 메모리는 모두 현재 프로세스가 쓰는 메모리이다.
1. VIRT
+ 프로세스가 사용하고 있는 virtual memory의 전체 용량
+ 프로세스에 할당된 가상 메모리 전체
+ SWAP + RES 로 계산된다.

2. RES
+ 현재 프로세스가 사용하고 있는 물리 메모리의 양
+ 실제로 메모리에 올려서 사용하고 있는 물리 메모리

3. SHR
+ 다른 프로세스와 공유하고 있는 shared memory의 양
