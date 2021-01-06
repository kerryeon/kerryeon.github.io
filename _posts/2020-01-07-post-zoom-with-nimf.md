---
title: "ArchLinux: nimf 입력기에서 zoom 한글 입력하기"
categories:
  - Blog
tags:
  - ArchLinux
  - zoom
  - nimf
---

[nimf](https://gitlab.com/nimf-i18n/nimf) 입력기를 사용하다, 언제부턴가 zoom 에서 한글입력이 안되는 문제가 발생했다.

[nimf](https://github.com/hamonikr/nimf) 는 [하모니카OS](https://hamonikr.org/)에서 포크한 버전을 사용중이다.

원인은, [zoom](https://zoom.us/) 을 빌드하면서 따라들어간 Qt 라이브러리에 있었던 것 같다.

먼저, 기존의 [zoom](https://aur.archlinux.org/packages/zoom/) 프로그램은 삭제하자. 나는 [yay AUR 도우미](https://github.com/Jguer/yay)로 설치하는 것을 선호한다.

``` bash
$ yay -Rns zoom
```

그 다음, [시스템의 Qt 라이브러리를 사용하는 버전](https://aur.archlinux.org/packages/zoom-system-qt/)으로 다시 설치한다.

``` bash
$ yay -S zoom-system-qt
```

![실행 영상](/assets/images/2020-01-07-image-01.jpg)

잘 입력된다.
