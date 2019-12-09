# WeeklyReport
 Highlight (Achievement)

#성균관대 MFL board개발
추가 문의 사항
A) 측정 시 500~1000point/sec 필요.
a. 현재 측정 결과 22528point/min 으로 초당 375point /sec로 측정됨.
b. 500mm/sec로 이동 시 1mm당 1point 이하 구간 발생 측정 안 되는 구간 생김.
c. MCU에서는 약750poin정도의 output이지만 실제 기록은 약 370point.
d. Ethernet의 속도 또는 interface의 속도 문제인지 다른 문제인지 형재 검토 중.
B) 기존 1분단위 저장 요구 했으나 Start와 stop구간을 모두 저장 하도록 요청
a. 고속 이동에는 1분단위도 이슈가 되지 않으나 저속 이동에는 1분단위 저장 시 전층 기록
불가
예) 15층 측정 시 고속 엘리베이터는 OK 저속은 5층정도까지만 기록 된다함.
data량 계산 후 성대 측에 알리고 저장 용량에 문제 없으면 구현 예정.
C) 저장 파일(*.csv)에서 헤더 제거  헤더에 문자 표기로 인한 오류 발생.
a. Time라인 추가 및 shift된 channel data 교정
D) 아래 사항에 대한 견적 요청
a. 원격 감시용 서버, UI개발 관련 견적 요청
현대 엘리베이터의 AWS서버 사용 불편
이에 따른 서버 구축, Matlab code변환, GUI등 개발 요청
b. 8채널용 무선 Mini DAQ제작 관련 견적 요청
엘리베이터용 Wire가 아니 엘리베이터용 chain 검사
Sensor header board에 일체형 DAQ설계.
LTE 통신 원함. --> 인증 문제로 인해 설계되는 보드위에 추가 하지 않고외부에 LTE Modem
부착
Battery 장착 문제 등 검토 필요
c. 80mm 케이블 이동 로봇 개발  진단용 이송 장치
현수교의 와이어에 MFL이동 장치 개발 고려중
Battery 장착 문제 등 검토 필요
MCDL
11월18일 설치 완료
A) 총 40대분 MCDL x 160pcs Sensor
a. 안산/전주 쉐플러 : 10pcs
b. 한미 정밀 화학: 12pcs
c. 대창: 5pcs
d. 대주: 3pcs
e. 현우: 5pcs
f. 오뚜기 식품: 3pcs
g. SMIC: 2pcs
B) 추가 작업:
a. 안산 쉐플러 제외 모든 site OS update 완료
금주 수요일(11월27일) 안산 쉐플러 업데이트 예정
b. SMIC network작업
외부 network 사용 불가, 내부 server와 MCDL까지의 LAN작업 필요

1층, 3층 LAN공사 완료
12월2일(월)_Network 동작 확인 예정_이은찬 상무
11월28일 작업 예정
c. Gateway 3pcs & Wireless Vibration sensor 10pcs준비 완료.
Issue
(1) DSP와 ARTIK간의 통신 문제
A. SPI
a. DSP: master, ARTIK: slave
b. TMS320F28379D에서 0x0000, 0xFFFF 데이터 반복 전송
B. ARTIK에서 정상 수신 안 됨
C. 원인: ARTIK에서 현재 사용중인 커널, 드라이버에서 Slave로 설정 못함
D. 커널 수정은 힘들고, 드라이버 수정 시도 중
E. DSP를 slave로 하는 방법은 관련 내용 검색 중(CPU는 다르지만 하나의 장비에서 SPI를 master,
slave 둘 다 설정 가능 한지)
(2) USB 및 MMC/SD card 접근 안됨.
a. 페도라 OS로 인해 동작 안함 엔지니어 의견
원인 파악 필요.
MCDL KC인증 준비
A) 인증 필요 문서 준비예정
미래융합의료기기
진행 사항
A) PCB입고 : 11월21일
B) 부품 입고 예정일: 11월27일
a. SMT완료 : 2019.11.29//PCBA입고 완료
