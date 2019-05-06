## openvpn-install
이 프로젝트는 https://github.com/Nyr/openvpn-install 에서 포크한 프로젝트입니다.

 HamoniKR Linux 에서 OpenVPN 설치를 쉽게 할 수 있는 방법을 제공하기 위해 만들어졌으며
 Debian, Ubuntu and CentOS 에서도 사용 가능합니다.

openvpn 을 모르는 경우에도 쉽게 설치가 가능하며, vpn 사용자를 추가하는 것도 아주 쉽게 가능합니다.

## 설치방법

아래와 같이 스크립트를 다운로드 받으신 후 루트 권한으로 실행하세요.

$ wget https://raw.githubusercontent.com/chaeya/openvpn-install/master/openvpn-install.sh -O openvpn-install.sh

$ sudo bash openvpn-install.sh

몇가지 선택을 하면 설치가 완료됩니다. 잘 모르는 경우 그냥 기본으로 선택된 값을 사용하세요

## vpn 사용자 추가

설치 후 서버에서 다시 스크립트를 실행하면 사용자를 쉽게 추가할 수 있습니다.

$ sudo bash openvpn-install.sh

스크립트 실행후 1번을 누르고 사용자명을 입력한 후 생성되는 ovpn 파일을 접속에 사용하도록 클라이언트에게 전달하세요.

## split tunnel

이 프로젝트는 모든 트래픽을 vpn으로 사용하지 않고 특정한 서비스만 vpn으로 사용하고 싶은 경우를 위한 설정이 반영되어 있습니다.
- 모든 트래픽을 vpn으로 사용하려는 경우에는 ovpn 확장자를 가진 클라이언트 설정파일의 2~5행을 삭제하면 됩니다.
- 원하는 서비스만 vpn 을 사용하려면 ovpn 확장자를 가진 클라이언트 설정파일의 5행 route 다음에 IP주소를 수정하세요.

