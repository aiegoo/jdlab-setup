Development configuration and project overview
## hardware spec and ubuntu setup

### mavlink, dronecode 
- install Ubuntu 18.04
- qt 5.15.2 [see below for more details](#qt)
- 


Do not use any other version of Qt! QGC has been thoroughly tested with the specified version of Qt (5.15.2). There is a significant risk that other Qt versions will inject bugs that affect stability and safety (even if QGC compiles).

- qt install and setup instructions
https://wiki.qt.io/Building_Qt_5_from_Git#Getting_the_source_code

perl init-repository
+ git submodule init qt3d qtactiveqt qtandroidextras qtbase qtcharts qtconnectivity qtdatavis3d qtdeclarative qtdoc qtgamepad qtgraphicaleffects qtimageformats qtlocation qtlottie qtmacextras qtmultimedia qtnetworkauth qtpurchasing qtqa qtquick3d qtquickcontrols qtquickcontrols2 qtquicktimeline qtremoteobjects qtrepotools qtscript qtscxml qtsensors qtserialbus qtserialport qtspeech qtsvg qttools qttranslations qtvirtualkeyboard qtwayland qtwebchannel qtwebengine qtwebglplugin qtwebsockets qtwebview qtwinextras qtx11extras qtxmlpatterns
'qt3d' 경로에 대해 'qt3d' (git://code.qt.io/qt/qt3d.git) 하위 모듈 등록
'qtactiveqt' 경로에 대해 'qtactiveqt' (git://code.qt.io/qt/qtactiveqt.git) 하위 모듈 등록
'qtandroidextras' 경로에 대해 'qtandroidextras' (git://code.qt.io/qt/qtandroidextras.git) 하위 모듈 등록
'qtbase' 경로에 대해 'qtbase' (git://code.qt.io/qt/qtbase.git) 하위 모듈 등록
'qtcharts' 경로에 대해 'qtcharts' (git://code.qt.io/qt/qtcharts.git) 하위 모듈 등록
'qtconnectivity' 경로에 대해 'qtconnectivity' (git://code.qt.io/qt/qtconnectivity.git) 하위 모듈 등록
'qtdatavis3d' 경로에 대해 'qtdatavis3d' (git://code.qt.io/qt/qtdatavis3d.git) 하위 모듈 등록
'qtdeclarative' 경로에 대해 'qtdeclarative' (git://code.qt.io/qt/qtdeclarative.git) 하위 모듈 등록
'qtdoc' 경로에 대해 'qtdoc' (git://code.qt.io/qt/qtdoc.git) 하위 모듈 등록
'qtgamepad' 경로에 대해 'qtgamepad' (git://code.qt.io/qt/qtgamepad.git) 하위 모듈 등록
'qtgraphicaleffects' 경로에 대해 'qtgraphicaleffects' (git://code.qt.io/qt/qtgraphicaleffects.git) 하위 모듈 등록
'qtimageformats' 경로에 대해 'qtimageformats' (git://code.qt.io/qt/qtimageformats.git) 하위 모듈 등록
'qtlocation' 경로에 대해 'qtlocation' (git://code.qt.io/qt/qtlocation.git) 하위 모듈 등록
'qtlottie' 경로에 대해 'qtlottie' (git://code.qt.io/qt/qtlottie.git) 하위 모듈 등록
'qtmacextras' 경로에 대해 'qtmacextras' (git://code.qt.io/qt/qtmacextras.git) 하위 모듈 등록
'qtmultimedia' 경로에 대해 'qtmultimedia' (git://code.qt.io/qt/qtmultimedia.git) 하위 모듈 등록
'qtnetworkauth' 경로에 대해 'qtnetworkauth' (git://code.qt.io/qt/qtnetworkauth.git) 하위 모듈 등록
'qtpurchasing' 경로에 대해 'qtpurchasing' (git://code.qt.io/qt/qtpurchasing.git) 하위 모듈 등록
'qtqa' 경로에 대해 'qtqa' (git://code.qt.io/qt/qtqa.git) 하위 모듈 등록
'qtquick3d' 경로에 대해 'qtquick3d' (git://code.qt.io/qt/qtquick3d.git) 하위 모듈 등록
'qtquickcontrols' 경로에 대해 'qtquickcontrols' (git://code.qt.io/qt/qtquickcontrols.git) 하위 모듈 등록
'qtquickcontrols2' 경로에 대해 'qtquickcontrols2' (git://code.qt.io/qt/qtquickcontrols2.git) 하위 모듈 등록
'qtquicktimeline' 경로에 대해 'qtquicktimeline' (git://code.qt.io/qt/qtquicktimeline) 하위 모듈 등록
'qtremoteobjects' 경로에 대해 'qtremoteobjects' (git://code.qt.io/qt/qtremoteobjects.git) 하위 모듈 등록
'qtrepotools' 경로에 대해 'qtrepotools' (git://code.qt.io/qt/qtrepotools.git) 하위 모듈 등록
'qtscript' 경로에 대해 'qtscript' (git://code.qt.io/qt/qtscript.git) 하위 모듈 등록
'qtscxml' 경로에 대해 'qtscxml' (git://code.qt.io/qt/qtscxml.git) 하위 모듈 등록
'qtsensors' 경로에 대해 'qtsensors' (git://code.qt.io/qt/qtsensors.git) 하위 모듈 등록
'qtserialbus' 경로에 대해 'qtserialbus' (git://code.qt.io/qt/qtserialbus.git) 하위 모듈 등록
'qtserialport' 경로에 대해 'qtserialport' (git://code.qt.io/qt/qtserialport.git) 하위 모듈 등록
'qtspeech' 경로에 대해 'qtspeech' (git://code.qt.io/qt/qtspeech.git) 하위 모듈 등록
'qtsvg' 경로에 대해 'qtsvg' (git://code.qt.io/qt/qtsvg.git) 하위 모듈 등록
'qttools' 경로에 대해 'qttools' (git://code.qt.io/qt/qttools.git) 하위 모듈 등록
'qttranslations' 경로에 대해 'qttranslations' (git://code.qt.io/qt/qttranslations.git) 하위 모듈 등록
'qtvirtualkeyboard' 경로에 대해 'qtvirtualkeyboard' (git://code.qt.io/qt/qtvirtualkeyboard.git) 하위 모듈 등록
'qtwayland' 경로에 대해 'qtwayland' (git://code.qt.io/qt/qtwayland.git) 하위 모듈 등록
'qtwebchannel' 경로에 대해 'qtwebchannel' (git://code.qt.io/qt/qtwebchannel.git) 하위 모듈 등록
'qtwebengine' 경로에 대해 'qtwebengine' (git://code.qt.io/qt/qtwebengine.git) 하위 모듈 등록
'qtwebglplugin' 경로에 대해 'qtwebglplugin' (git://code.qt.io/qt/qtwebglplugin.git) 하위 모듈 등록
'qtwebsockets' 경로에 대해 'qtwebsockets' (git://code.qt.io/qt/qtwebsockets.git) 하위 모듈 등록
'qtwebview' 경로에 대해 'qtwebview' (git://code.qt.io/qt/qtwebview.git) 하위 모듈 등록
'qtwinextras' 경로에 대해 'qtwinextras' (git://code.qt.io/qt/qtwinextras.git) 하위 모듈 등록
'qtx11extras' 경로에 대해 'qtx11extras' (git://code.qt.io/qt/qtx11extras.git) 하위 모듈 등록
'qtxmlpatterns' 경로에 대해 'qtxmlpatterns' (git://code.qt.io/qt/qtxmlpatterns.git) 하위 모듈 등록
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git clone --no-checkout git://code.qt.io/qt/qt3d.git qt3d
'qt3d'에 복제합니다...
remote: Counting objects: 132227, done.
remote: Compressing objects: 100% (14077/14077), done.
remote: Total 132227 (delta 18748), reused 12751 (delta 9635)
오브젝트를 받는 중: 100% (132227/132227), 156.86 MiB | 341.00 KiB/s, 완료.
델타를 알아내는 중: 100% (105400/105400), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qt3d.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtactiveqt.git qtactiveqt
'qtactiveqt'에 복제합니다...
remote: Counting objects: 9593, done.
remote: Compressing objects: 100% (7125/7125), done.
remote: Total 9593 (delta 5878), reused 3621 (delta 2275)
오브젝트를 받는 중: 100% (9593/9593), 2.32 MiB | 313.00 KiB/s, 완료.
델타를 알아내는 중: 100% (5878/5878), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtactiveqt.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtandroidextras.git qtandroidextras
'qtandroidextras'에 복제합니다...
remote: Counting objects: 3160, done.
remote: Compressing objects: 100% (2647/2647), done.
remote: Total 3160 (delta 1632), reused 714 (delta 296)
오브젝트를 받는 중: 100% (3160/3160), 790.78 KiB | 171.00 KiB/s, 완료.
델타를 알아내는 중: 100% (1632/1632), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtandroidextras.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtbase.git qtbase
'qtbase'에 복제합니다...
remote: Counting objects: 759133, done.
remote: Compressing objects: 100% (129501/129501), done.
remote: Total 759133 (delta 624443), reused 754510 (delta 621801)
오브젝트를 받는 중: 100% (759133/759133), 280.46 MiB | 284.00 KiB/s, 완료.
델타를 알아내는 중: 100% (624443/624443), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtbase.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtcharts.git qtcharts
'qtcharts'에 복제합니다...
remote: Counting objects: 49795, done.
remote: Compressing objects: 100% (12950/12950), done.
remote: Total 49795 (delta 39292), reused 45897 (delta 36202)
오브젝트를 받는 중: 100% (49795/49795), 18.98 MiB | 245.00 KiB/s, 완료.
델타를 알아내는 중: 100% (39292/39292), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtcharts.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtconnectivity.git qtconnectivity
'qtconnectivity'에 복제합니다...
remote: Counting objects: 31074, done.
remote: Compressing objects: 100% (9163/9163), done.
remote: Total 31074 (delta 22883), reused 28489 (delta 21000)
오브젝트를 받는 중: 100% (31074/31074), 11.77 MiB | 479.00 KiB/s, 완료.
델타를 알아내는 중: 100% (22883/22883), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtconnectivity.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtdatavis3d.git qtdatavis3d
'qtdatavis3d'에 복제합니다...
remote: Counting objects: 30196, done.
remote: Compressing objects: 100% (10386/10386), done.
remote: Total 30196 (delta 22788), reused 24297 (delta 18753)
오브젝트를 받는 중: 100% (30196/30196), 38.78 MiB | 976.00 KiB/s, 완료.
델타를 알아내는 중: 100% (22788/22788), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtdatavis3d.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtdeclarative.git qtdeclarative
'qtdeclarative'에 복제합니다...
remote: Counting objects: 398534, done.
remote: Compressing objects: 100% (35558/35558), done.
remote: Total 398534 (delta 83663), reused 99268 (delta 74037)
오브젝트를 받는 중: 100% (398534/398534), 133.27 MiB | 447.00 KiB/s, 완료.
델타를 알아내는 중: 100% (320496/320496), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtdeclarative.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtdoc.git qtdoc
'qtdoc'에 복제합니다...
remote: Counting objects: 33940, done.
remote: Compressing objects: 100% (10987/10987), done.
remote: Total 33940 (delta 23950), reused 31887 (delta 22434)
오브젝트를 받는 중: 100% (33940/33940), 46.06 MiB | 584.00 KiB/s, 완료.
델타를 알아내는 중: 100% (23950/23950), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtdoc.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtgamepad.git qtgamepad
'qtgamepad'에 복제합니다...
remote: Counting objects: 2126, done.
remote: Compressing objects: 100% (2027/2027), done.
remote: Total 2126 (delta 1146), reused 80 (delta 25)
오브젝트를 받는 중: 100% (2126/2126), 667.79 KiB | 118.00 KiB/s, 완료.
델타를 알아내는 중: 100% (1146/1146), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtgamepad.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtgraphicaleffects.git qtgraphicaleffects
'qtgraphicaleffects'에 복제합니다...
remote: Counting objects: 5740, done.
remote: Compressing objects: 100% (3487/3487), done.
remote: Total 5740 (delta 3472), reused 3411 (delta 2120)
오브젝트를 받는 중: 100% (5740/5740), 31.39 MiB | 692.00 KiB/s, 완료.
델타를 알아내는 중: 100% (3472/3472), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtgraphicaleffects.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtimageformats.git qtimageformats
'qtimageformats'에 복제합니다...
remote: Counting objects: 9502, done.
remote: Compressing objects: 100% (8241/8241), done.
remote: Total 9502 (delta 5597), reused 2447 (delta 1089)
오브젝트를 받는 중: 100% (9502/9502), 6.21 MiB | 388.00 KiB/s, 완료.
델타를 알아내는 중: 100% (5597/5597), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtimageformats.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtlocation.git qtlocation
'qtlocation'에 복제합니다...
remote: Counting objects: 54594, done.
remote: Compressing objects: 100% (19790/19790), done.
remote: Total 54594 (delta 41539), reused 44401 (delta 34123)
오브젝트를 받는 중: 100% (54594/54594), 22.83 MiB | 1.17 MiB/s, 완료.
델타를 알아내는 중: 100% (41539/41539), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtlocation.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtlottie.git qtlottie
'qtlottie'에 복제합니다...
remote: Counting objects: 2436, done.
remote: Compressing objects: 100% (2297/2297), done.
remote: Total 2436 (delta 1598), reused 175 (delta 122)
오브젝트를 받는 중: 100% (2436/2436), 382.07 KiB | 94.00 KiB/s, 완료.
델타를 알아내는 중: 100% (1598/1598), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtlottie.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtmacextras.git qtmacextras
'qtmacextras'에 복제합니다...
remote: Counting objects: 2454, done.
remote: Compressing objects: 100% (1708/1708), done.
remote: Total 2454 (delta 1350), reused 1109 (delta 659)
오브젝트를 받는 중: 100% (2454/2454), 609.25 KiB | 91.00 KiB/s, 완료.
델타를 알아내는 중: 100% (1350/1350), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtmacextras.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtmultimedia.git qtmultimedia
'qtmultimedia'에 복제합니다...
remote: Counting objects: 76756, done.
remote: Compressing objects: 100% (7370/7370), done.
remote: Total 76756 (delta 14624), reused 12868 (delta 10344)
오브젝트를 받는 중: 100% (76756/76756), 25.96 MiB | 779.00 KiB/s, 완료.
델타를 알아내는 중: 100% (62517/62517), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtmultimedia.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtnetworkauth.git qtnetworkauth
'qtnetworkauth'에 복제합니다...
remote: Counting objects: 4535, done.
remote: Compressing objects: 100% (4508/4508), done.
remote: Total 4535 (delta 2726), reused 0 (delta 0)
오브젝트를 받는 중: 100% (4535/4535), 673.88 KiB | 170.00 KiB/s, 완료.
델타를 알아내는 중: 100% (2726/2726), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtnetworkauth.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtpurchasing.git qtpurchasing
'qtpurchasing'에 복제합니다...
remote: Counting objects: 2653, done.
remote: Compressing objects: 100% (1951/1951), done.
remote: Total 2653 (delta 1542), reused 951 (delta 580)
오브젝트를 받는 중: 100% (2653/2653), 600.00 KiB | 167.00 KiB/s, 완료.
델타를 알아내는 중: 100% (1542/1542), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtpurchasing.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtqa.git qtqa
'qtqa'에 복제합니다...
remote: Counting objects: 11061, done.
remote: Compressing objects: 100% (7227/7227), done.
remote: Total 11061 (delta 6995), reused 5199 (delta 3358)
오브젝트를 받는 중: 100% (11061/11061), 15.34 MiB | 341.00 KiB/s, 완료.
델타를 알아내는 중: 100% (6995/6995), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtqa.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtquick3d.git qtquick3d
'qtquick3d'에 복제합니다...
remote: Counting objects: 37412, done.
remote: Compressing objects: 100% (15664/15664), done.
remote: Total 37412 (delta 29217), reused 28194 (delta 21610)
오브젝트를 받는 중: 100% (37412/37412), 54.66 MiB | 548.00 KiB/s, 완료.
델타를 알아내는 중: 100% (29217/29217), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtquick3d.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtquickcontrols.git qtquickcontrols
'qtquickcontrols'에 복제합니다...
remote: Counting objects: 34270, done.
remote: Compressing objects: 100% (14794/14794), done.
remote: Total 34270 (delta 24192), reused 26344 (delta 19002)
오브젝트를 받는 중: 100% (34270/34270), 14.70 MiB | 855.00 KiB/s, 완료.
델타를 알아내는 중: 100% (24192/24192), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtquickcontrols.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtquickcontrols2.git qtquickcontrols2
'qtquickcontrols2'에 복제합니다...
remote: Counting objects: 68528, done.
remote: Compressing objects: 100% (9734/9734), done.
remote: Total 68528 (delta 13469), reused 12016 (delta 8514)
오브젝트를 받는 중: 100% (68528/68528), 27.43 MiB | 498.00 KiB/s, 완료.
델타를 알아내는 중: 100% (50518/50518), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtquickcontrols2.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtquicktimeline qtquicktimeline
'qtquicktimeline'에 복제합니다...
remote: Counting objects: 3822, done.
remote: Compressing objects: 100% (3721/3721), done.
remote: Total 3822 (delta 2456), reused 148 (delta 62)
오브젝트를 받는 중: 100% (3822/3822), 532.67 KiB | 108.00 KiB/s, 완료.
델타를 알아내는 중: 100% (2456/2456), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtquicktimeline
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtremoteobjects.git qtremoteobjects
'qtremoteobjects'에 복제합니다...
remote: Counting objects: 11690, done.
remote: Compressing objects: 100% (5274/5274), done.
remote: Total 11690 (delta 7893), reused 9625 (delta 6332)
오브젝트를 받는 중: 100% (11690/11690), 2.40 MiB | 249.00 KiB/s, 완료.
델타를 알아내는 중: 100% (7893/7893), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtremoteobjects.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtrepotools.git qtrepotools
'qtrepotools'에 복제합니다...

remote: Counting objects: 3565, done.
remote: Compressing objects: 100% (1903/1903), done.
remote: Total 3565 (delta 2406), reused 2328 (delta 1511)
오브젝트를 받는 중: 100% (3565/3565), 889.54 KiB | 126.00 KiB/s, 완료.
델타를 알아내는 중: 100% (2406/2406), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtrepotools.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtscript.git qtscript
'qtscript'에 복제합니다...
remote: Counting objects: 12076, done.
remote: Compressing objects: 100% (5298/5298), done.
remote: Total 12076 (delta 7756), reused 9822 (delta 6481)
오브젝트를 받는 중: 100% (12076/12076), 10.83 MiB | 289.00 KiB/s, 완료.
델타를 알아내는 중: 100% (7756/7756), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtscript.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtscxml.git qtscxml
'qtscxml'에 복제합니다...
remote: Counting objects: 13251, done.
remote: Compressing objects: 100% (9419/9419), done.
remote: Total 13251 (delta 8638), reused 5385 (delta 3585)
오브젝트를 받는 중: 100% (13251/13251), 4.06 MiB | 549.00 KiB/s, 완료.
델타를 알아내는 중: 100% (8638/8638), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtscxml.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtsensors.git qtsensors
'qtsensors'에 복제합니다...
remote: Counting objects: 15886, done.
remote: Compressing objects: 100% (8261/8261), done.
remote: Total 15886 (delta 10791), reused 10327 (delta 7275)
오브젝트를 받는 중: 100% (15886/15886), 6.38 MiB | 350.00 KiB/s, 완료.
델타를 알아내는 중: 100% (10791/10791), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtsensors.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtserialbus.git qtserialbus
'qtserialbus'에 복제합니다...
remote: Counting objects: 14064, done.
remote: Compressing objects: 100% (6558/6558), done.
remote: Total 14064 (delta 9101), reused 11770 (delta 7436)
오브젝트를 받는 중: 100% (14064/14064), 2.48 MiB | 201.00 KiB/s, 완료.
델타를 알아내는 중: 100% (9101/9101), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtserialbus.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtserialport.git qtserialport
'qtserialport'에 복제합니다...
remote: Counting objects: 11777, done.
remote: Compressing objects: 100% (7057/7057), done.
remote: Total 11777 (delta 7640), reused 6808 (delta 4601)
오브젝트를 받는 중: 100% (11777/11777), 2.83 MiB | 314.00 KiB/s, 완료.
델타를 알아내는 중: 100% (7640/7640), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtserialport.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtspeech.git qtspeech
'qtspeech'에 복제합니다...
remote: Counting objects: 2944, done.
remote: Compressing objects: 100% (2587/2587), done.
remote: Total 2944 (delta 1688), reused 376 (delta 212)
오브젝트를 받는 중: 100% (2944/2944), 539.12 KiB | 149.00 KiB/s, 완료.
델타를 알아내는 중: 100% (1688/1688), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtspeech.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtsvg.git qtsvg
'qtsvg'에 복제합니다...
remote: Counting objects: 10862, done.
remote: Compressing objects: 100% (8625/8625), done.
remote: Total 10862 (delta 6896), reused 3317 (delta 2067)
오브젝트를 받는 중: 100% (10862/10862), 4.50 MiB | 392.00 KiB/s, 완료.
델타를 알아내는 중: 100% (6896/6896), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtsvg.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qttools.git qttools
'qttools'에 복제합니다...
remote: Counting objects: 64373, done.
remote: Compressing objects: 100% (19289/19289), done.
remote: Total 64373 (delta 50458), reused 57613 (delta 44574)
오브젝트를 받는 중: 100% (64373/64373), 32.64 MiB | 655.00 KiB/s, 완료.
델타를 알아내는 중: 100% (50458/50458), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qttools.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qttranslations.git qttranslations
'qttranslations'에 복제합니다...
remote: Counting objects: 5830, done.
remote: Compressing objects: 100% (4951/4951), done.
remote: Total 5830 (delta 3981), reused 1029 (delta 780)
오브젝트를 받는 중: 100% (5830/5830), 8.98 MiB | 638.00 KiB/s, 완료.
델타를 알아내는 중: 100% (3981/3981), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qttranslations.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtvirtualkeyboard.git qtvirtualkeyboard
'qtvirtualkeyboard'에 복제합니다...
remote: Counting objects: 16998, done.
remote: Compressing objects: 100% (6955/6955), done.
remote: Total 16998 (delta 11879), reused 14430 (delta 9772)
오브젝트를 받는 중: 100% (16998/16998), 16.64 MiB | 444.00 KiB/s, 완료.
델타를 알아내는 중: 100% (11879/11879), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtvirtualkeyboard.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtwayland.git qtwayland
'qtwayland'에 복제합니다...
remote: Counting objects: 44923, done.
remote: Compressing objects: 100% (15002/15002), done.
remote: Total 44923 (delta 33200), reused 39536 (delta 28889)
오브젝트를 받는 중: 100% (44923/44923), 9.13 MiB | 402.00 KiB/s, 완료.
델타를 알아내는 중: 100% (33200/33200), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtwayland.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtwebchannel.git qtwebchannel
'qtwebchannel'에 복제합니다...
remote: Counting objects: 5522, done.
remote: Compressing objects: 100% (4240/4240), done.
remote: Total 5522 (delta 3464), reused 1853 (delta 1167)
오브젝트를 받는 중: 100% (5522/5522), 1.20 MiB | 214.00 KiB/s, 완료.
델타를 알아내는 중: 100% (3464/3464), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtwebchannel.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtwebengine.git qtwebengine
'qtwebengine'에 복제합니다...
remote: Counting objects: 64345, done.
remote: Compressing objects: 100% (4793/4793), done.
remote: Total 64345 (delta 3617), reused 339 (delta 177)
오브젝트를 받는 중: 100% (64345/64345), 15.53 MiB | 1.07 MiB/s, 완료.
델타를 알아내는 중: 100% (50584/50584), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtwebengine.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtwebglplugin.git qtwebglplugin
'qtwebglplugin'에 복제합니다...
remote: Counting objects: 1334, done.
remote: Compressing objects: 100% (1293/1293), done.
remote: Total 1334 (delta 577), reused 0 (delta 0)
오브젝트를 받는 중: 100% (1334/1334), 261.24 KiB | 128.00 KiB/s, 완료.
델타를 알아내는 중: 100% (577/577), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtwebglplugin.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtwebsockets.git qtwebsockets
'qtwebsockets'에 복제합니다...
remote: Counting objects: 8719, done.
remote: Compressing objects: 100% (6114/6114), done.
remote: Total 8719 (delta 5944), reused 3695 (delta 2535)
오브젝트를 받는 중: 100% (8719/8719), 2.10 MiB | 248.00 KiB/s, 완료.
델타를 알아내는 중: 100% (5944/5944), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtwebsockets.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtwebview.git qtwebview
'qtwebview'에 복제합니다...
remote: Counting objects: 3796, done.
remote: Compressing objects: 100% (3300/3300), done.
remote: Total 3796 (delta 2213), reused 628 (delta 311)
오브젝트를 받는 중: 100% (3796/3796), 821.38 KiB | 146.00 KiB/s, 완료.
델타를 알아내는 중: 100% (2213/2213), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtwebview.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtwinextras.git qtwinextras
'qtwinextras'에 복제합니다...
remote: Counting objects: 4051, done.
remote: Compressing objects: 100% (2788/2788), done.
remote: Total 4051 (delta 2437), reused 1859 (delta 1154)
오브젝트를 받는 중: 100% (4051/4051), 1.95 MiB | 383.00 KiB/s, 완료.
델타를 알아내는 중: 100% (2437/2437), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtwinextras.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtx11extras.git qtx11extras
'qtx11extras'에 복제합니다...
remote: Counting objects: 1567, done.
remote: Compressing objects: 100% (1362/1362), done.
remote: Total 1567 (delta 732), reused 391 (delta 148)
오브젝트를 받는 중: 100% (1567/1567), 450.40 KiB | 71.00 KiB/s, 완료.
델타를 알아내는 중: 100% (732/732), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtx11extras.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git clone --no-checkout git://code.qt.io/qt/qtxmlpatterns.git qtxmlpatterns
'qtxmlpatterns'에 복제합니다...
remote: Counting objects: 16992, done.
remote: Compressing objects: 100% (5053/5053), done.
remote: Total 16992 (delta 13690), reused 13778 (delta 11650)
오브젝트를 받는 중: 100% (16992/16992), 8.09 MiB | 508.00 KiB/s, 완료.
델타를 알아내는 중: 100% (13690/13690), 완료.
+ git config commit.template /home/aiegoo/repos/projects/qt5/.commit-template
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtxmlpatterns.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git submodule update --force --no-fetch
하위 모듈 경로 'qt3d': '077b1281ca376a39a5815b112e8e067cdc9165f4' 체크아웃
하위 모듈 경로 'qtactiveqt': 'f0d03da0e37a84029a4eae1733813521482ac1fb' 체크아웃
하위 모듈 경로 'qtandroidextras': '8cce1098c59534352aa0f343ea73861f603ac04a' 체크아웃
하위 모듈 경로 'qtbase': 'ffa0ecdc5d507754ddd962e2edbc859c198b2700' 체크아웃
하위 모듈 경로 'qtcharts': '130463160b4923069eb98da49edaf7d93180f4f8' 체크아웃
하위 모듈 경로 'qtconnectivity': '69a87a9b831e36a578594a0a13130c384ad03121' 체크아웃
하위 모듈 경로 'qtdatavis3d': 'c085311c02dd216e5a041b90c164d55b3cf3ce92' 체크아웃
하위 모듈 경로 'qtdeclarative': '35614462443c100b6753b335b58a134fed4b5c35' 체크아웃
하위 모듈 경로 'qtdoc': '897e90fe304d844beaf694b82a93a50237fa8b9e' 체크아웃
하위 모듈 경로 'qtgamepad': '64afa18a0a1e9588060e2e6d917bb01ccdd48a81' 체크아웃
하위 모듈 경로 'qtgraphicaleffects': 'c36998dc1581167b12cc3de8e4ac68c2a5d9f76e' 체크아웃
하위 모듈 경로 'qtimageformats': 'cb82c74310837fe4e832c8ab72176a5d63e4355f' 체크아웃
하위 모듈 경로 'qtlocation': '861e372b6ad81570d4f496e42fb25a6699b72f2f' 체크아웃
하위 모듈 경로 'qtlottie': 'fa8c8bfc6742ab98b61d1351e054e0e73e9a42f4' 체크아웃
하위 모듈 경로 'qtmacextras': 'e72896968697e2a8af16a312e1560948e4c40f30' 체크아웃
하위 모듈 경로 'qtmultimedia': 'bd29c87027637a013f2c5e3b549fcda84e4d7545' 체크아웃
하위 모듈 경로 'qtnetworkauth': '53870ee9bb9117702cd1f11cb1c5d1cfc2d5394a' 체크아웃
하위 모듈 경로 'qtpurchasing': 'cbf444fb570ca4f4ca21d963d2ae4010f10d473e' 체크아웃
하위 모듈 경로 'qtqa': '36da1912a90c0e3a91f59f96c984a7e43ab982b7' 체크아웃
하위 모듈 경로 'qtquick3d': 'de162f30e8fd23b5fa45ffef0752aab8540129f3' 체크아웃
하위 모듈 경로 'qtquickcontrols': 'cf3f6d7fec824cdf01f9b329ab3b92b1c0e0a420' 체크아웃
하위 모듈 경로 'qtquickcontrols2': 'a2593ff9cf5d0af885c20c2e9f9faa6ca4f1c1a3' 체크아웃
하위 모듈 경로 'qtquicktimeline': '67503cdadea43b95ddad0de1a04951aff0ce1a07' 체크아웃
하위 모듈 경로 'qtremoteobjects': '4d6d1e35fb8e0cb900b5e5e9266edea51dc4f735' 체크아웃
하위 모듈 경로 'qtrepotools': 'ee34618d9f94e0cb6f678140e6cd2916308531b5' 체크아웃
하위 모듈 경로 'qtscript': '5be95f966aabc5170f0aacfd4b0a46217241bfd6' 체크아웃
하위 모듈 경로 'qtscxml': '7a15000f42c7a3171719727cd056f82a78244ed7' 체크아웃
하위 모듈 경로 'qtsensors': '921a31375f29e429e95352b08b2b9dbfea663cb1' 체크아웃
하위 모듈 경로 'qtserialbus': '8884c5e43df846deac5a0c7c290eeb633d6bfe32' 체크아웃
하위 모듈 경로 'qtserialport': '941d1d8560d1f3e40077c251fbde6fd6a5b0f0d4' 체크아웃
하위 모듈 경로 'qtspeech': 'a0efc38377e5bf7eed2d354d1cb4d7a0d5dc7e1b' 체크아웃
하위 모듈 경로 'qtsvg': 'aceea78cc05ac8ff947cee9de8149b48771781a8' 체크아웃
하위 모듈 경로 'qttools': '33693a928986006d79c1ee743733cde5966ac402' 체크아웃
하위 모듈 경로 'qttranslations': '68f420ebdfb226e3d0c09ebed06d5454cc6c3a7f' 체크아웃
하위 모듈 경로 'qtvirtualkeyboard': '2f0e9f98c6c6fdac09f762d41fddcc114f64b28a' 체크아웃
하위 모듈 경로 'qtwayland': 'a8d35b3c18bdb05a0da3ed50a554a7b7bd4ebed3' 체크아웃
하위 모듈 경로 'qtwebchannel': '47be9a51b01d9fd9e7f6dca81e98d4eedcec6d38' 체크아웃
하위 모듈 경로 'qtwebengine': 'f328054d2eafc073b98a0246b2d644ee09c99d9c' 체크아웃
하위 모듈 경로 'qtwebglplugin': '550a8cee241bbf8c11863dec9587d579dcb1108b' 체크아웃
하위 모듈 경로 'qtwebsockets': 'e7883bc64440b1ff4666272ac6eb710ee4bc221b' 체크아웃
하위 모듈 경로 'qtwebview': '920de5f1cd9f9001cfef1bfd2c19e6720793362f' 체크아웃
하위 모듈 경로 'qtwinextras': '3df03dab21f3e84d5a7274c64dd879854ca1bfe7' 체크아웃
하위 모듈 경로 'qtx11extras': '3898f5484fd4864b047729bfeda9a1222f32364f' 체크아웃
하위 모듈 경로 'qtxmlpatterns': '189e28d0aff1f3d7960228ba318b83e3cadac98c' 체크아웃
+ git submodule init tests/auto/qml/ecmascripttests/test262
'tests/auto/qml/ecmascripttests/test262' 경로에 대해 'tests/auto/qml/ecmascripttests/test262' (git://code.qt.io/qt/qtdeclarative-testsuites.git) 하위 모듈 등록
 *** /qtdeclarative/tests/auto/qml/ecmascripttests/test262 not found, ignoring alternate for this submodule
+ git clone --no-checkout git://code.qt.io/qt/qtdeclarative-testsuites.git tests/auto/qml/ecmascripttests/test262
'tests/auto/qml/ecmascripttests/test262'에 복제합니다...
remote: Counting objects: 238777, done.
remote: Compressing objects: 100% (132027/132027), done.
remote: Total 238777 (delta 105729), reused 238664 (delta 105694)
오브젝트를 받는 중: 100% (238777/238777), 168.65 MiB | 1.49 MiB/s, 완료.
델타를 알아내는 중: 100% (105729/105729), 완료.
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtdeclarative-testsuites.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git submodule update --force --no-fetch
하위 모듈 경로 'tests/auto/qml/ecmascripttests/test262': '6b0c42c63c2492bd0a7a96d3179d122b5f71793f' 체크아웃
+ git submodule init src/3rdparty/mapbox-gl-native
'src/3rdparty/mapbox-gl-native' 경로에 대해 'src/3rdparty/mapbox-gl-native' (git://code.qt.io/qt/qtlocation-mapboxgl.git) 하위 모듈 등록
 *** /qtlocation/src/3rdparty/mapbox-gl-native not found, ignoring alternate for this submodule
+ git clone --no-checkout git://code.qt.io/qt/qtlocation-mapboxgl.git src/3rdparty/mapbox-gl-native
'src/3rdparty/mapbox-gl-native'에 복제합니다...
remote: Counting objects: 241401, done.
remote: Compressing objects: 100% (56154/56154), done.
remote: Total 241401 (delta 168714), reused 240107 (delta 168002)
오브젝트를 받는 중: 100% (241401/241401), 328.59 MiB | 3.87 MiB/s, 완료.
델타를 알아내는 중: 100% (168714/168714), 완료.
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtlocation-mapboxgl.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git submodule update --force --no-fetch
하위 모듈 경로 'src/3rdparty/mapbox-gl-native': 'd3101bbc22edd41c9036ea487d4a71eabd97823d' 체크아웃
+ git submodule init src/3rdparty/assimp/src
'src/3rdparty/assimp/src' 경로에 대해 'src/3rdparty/assimp/src' (git://code.qt.io/qt/qtquick3d-assimp.git) 하위 모듈 등록
 *** /qtquick3d/src/3rdparty/assimp/src not found, ignoring alternate for this submodule
+ git clone --no-checkout git://code.qt.io/qt/qtquick3d-assimp.git src/3rdparty/assimp/src
'src/3rdparty/assimp/src'에 복제합니다...
remote: Counting objects: 71003, done.
remote: Compressing objects: 100% (26765/26765), done.
remote: Total 71003 (delta 51887), reused 59543 (delta 42619)
오브젝트를 받는 중: 100% (71003/71003), 177.02 MiB | 3.17 MiB/s, 완료.
델타를 알아내는 중: 100% (51887/51887), 완료.
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtquick3d-assimp.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git submodule update --force --no-fetch
하위 모듈 경로 'src/3rdparty/assimp/src': '8f0c6b04b2257a520aaab38421b2e090204b69df' 체크아웃
+ git submodule init src/3rdparty
'src/3rdparty' 경로에 대해 'src/3rdparty' (git://code.qt.io/qt/qtwebengine-chromium.git) 하위 모듈 등록
 *** /qtwebengine/src/3rdparty not found, ignoring alternate for this submodule
+ git clone --no-checkout git://code.qt.io/qt/qtwebengine-chromium.git src/3rdparty
'src/3rdparty'에 복제합니다...
remote: Counting objects: 1725036, done.
remote: Compressing objects: 100% (1868/1868), done.
remote: Total 1725036 (delta 1097), reused 102 (delta 53)
오브젝트를 받는 중: 100% (1725036/1725036), 1.86 GiB | 2.08 MiB/s, 완료.
델타를 알아내는 중: 100% (1309976/1309976), 완료.
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtwebengine-chromium.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git submodule update --force --no-fetch
하위 모듈 경로 'src/3rdparty': '25db271c9b53e576cbb2cdc84d2c56ca5e8633a8' 체크아웃
+ git submodule init tests/auto/3rdparty/testsuites
'tests/auto/3rdparty/testsuites' 경로에 대해 'testsuites' (git://code.qt.io/qt/qtxmlpatterns-testsuites.git) 하위 모듈 등록
 *** /qtxmlpatterns/tests/auto/3rdparty/testsuites not found, ignoring alternate for this submodule
+ git clone --no-checkout git://code.qt.io/qt/qtxmlpatterns-testsuites.git tests/auto/3rdparty/testsuites
'tests/auto/3rdparty/testsuites'에 복제합니다...
remote: Counting objects: 44057, done.
remote: Compressing objects: 100% (9930/9930), done.
remote: Total 44057 (delta 31795), reused 44057 (delta 31795)
오브젝트를 받는 중: 100% (44057/44057), 12.43 MiB | 925.00 KiB/s, 완료.
델타를 알아내는 중: 100% (31795/31795), 완료.
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qtxmlpatterns-testsuites.git
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
+ git submodule update --force --no-fetch
하위 모듈 경로 'tests/auto/3rdparty/testsuites': 'ddfcd98e8d3f78d696bb25ddcaacc3e3cba51e7f' 체크아웃
+ git config remote.gerrit.url ssh://codereview.qt-project.org/qt/qt5
+ git config remote.gerrit.fetch +refs/heads/*:refs/remotes/gerrit/* /heads/
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qt3d/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qt3d/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtactiveqt/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtactiveqt/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtandroidextras/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtandroidextras/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtbase/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtbase/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtcharts/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtcharts/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtconnectivity/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtconnectivity/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtdatavis3d/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtdatavis3d/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtdeclarative/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtdeclarative/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtdoc/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtdoc/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtgamepad/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtgamepad/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtgraphicaleffects/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtgraphicaleffects/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtimageformats/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtimageformats/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtlocation/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtlocation/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtlottie/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtlottie/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtmacextras/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtmacextras/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtmultimedia/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtmultimedia/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtnetworkauth/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtnetworkauth/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtpurchasing/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtpurchasing/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtqa/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtqa/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtquick3d/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtquick3d/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtquickcontrols/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtquickcontrols/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtquickcontrols2/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtquickcontrols2/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtquicktimeline/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtquicktimeline/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtremoteobjects/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtremoteobjects/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtrepotools/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtrepotools/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtscript/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtscript/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtscxml/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtscxml/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtsensors/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtsensors/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtserialbus/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtserialbus/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtserialport/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtserialport/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtspeech/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtspeech/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtsvg/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtsvg/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qttools/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qttools/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qttranslations/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qttranslations/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtvirtualkeyboard/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtvirtualkeyboard/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtwayland/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtwayland/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtwebchannel/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtwebchannel/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtwebengine/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtwebengine/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtwebglplugin/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtwebglplugin/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtwebsockets/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtwebsockets/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtwebview/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtwebview/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtwinextras/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtwinextras/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtx11extras/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtx11extras/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtxmlpatterns/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtxmlpatterns/.git/hooks/post-commit ...
aiegoo@tonylee:~/repos/projects/qt5$ 
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtmultimedia/.git/hooks/commit-msg ...
qtmultimedia/.git/hooks/commit-msg: Assembler messages:
qtmultimedia/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtmultimedia/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtmultimedia/.git/hooks/commit-msg:29: Error: bad expression
qtmultimedia/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtmultimedia/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtmultimedia/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtmultimedia/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtmultimedia/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtmultimedia/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtmultimedia/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtmultimedia/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtmultimedia/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtmultimedia/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtmultimedia/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtmultimedia/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtmultimedia/.git/hooks/commit-msg:47: Error: bad expression
qtmultimedia/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtmultimedia/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtmultimedia/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtmultimedia/.git/hooks/commit-msg:52: Error: bad expression
qtmultimedia/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtmultimedia/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtmultimedia/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtmultimedia/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtmultimedia/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtmultimedia/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtmultimedia/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtmultimedia/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtmultimedia/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtmultimedia/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtmultimedia/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtmultimedia/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtmultimedia/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtmultimedia/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtmultimedia/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtmultimedia/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtmultimedia/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtmultimedia/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtmultimedia/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtmultimedia/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtmultimedia/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtmultimedia/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtmultimedia/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtmultimedia/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtmultimedia/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtmultimedia/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtmultimedia/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtmultimedia/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtmultimedia/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtmultimedia/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtmultimedia/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtmultimedia/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtmultimedia/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtmultimedia/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtmultimedia/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtmultimedia/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtmultimedia/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtmultimedia/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtmultimedia/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtmultimedia/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtmultimedia/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtmultimedia/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtmultimedia/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtmultimedia/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtmultimedia/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtmultimedia/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtmultimedia/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtmultimedia/.git/hooks/post-commit ...
qtmultimedia/.git/hooks/post-commit: Assembler messages:
qtmultimedia/.git/hooks/post-commit: Warning: end of file in comment
qtmultimedia/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtmultimedia/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtmultimedia/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtnetworkauth/.git/hooks/commit-msg ...
qtnetworkauth/.git/hooks/commit-msg: Assembler messages:
qtnetworkauth/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtnetworkauth/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtnetworkauth/.git/hooks/commit-msg:29: Error: bad expression
qtnetworkauth/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtnetworkauth/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtnetworkauth/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtnetworkauth/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtnetworkauth/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtnetworkauth/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtnetworkauth/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtnetworkauth/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtnetworkauth/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtnetworkauth/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtnetworkauth/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtnetworkauth/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtnetworkauth/.git/hooks/commit-msg:47: Error: bad expression
qtnetworkauth/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtnetworkauth/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtnetworkauth/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtnetworkauth/.git/hooks/commit-msg:52: Error: bad expression
qtnetworkauth/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtnetworkauth/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtnetworkauth/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtnetworkauth/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtnetworkauth/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtnetworkauth/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtnetworkauth/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtnetworkauth/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtnetworkauth/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtnetworkauth/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtnetworkauth/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtnetworkauth/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtnetworkauth/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtnetworkauth/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtnetworkauth/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtnetworkauth/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtnetworkauth/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtnetworkauth/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtnetworkauth/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtnetworkauth/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtnetworkauth/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtnetworkauth/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtnetworkauth/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtnetworkauth/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtnetworkauth/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtnetworkauth/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtnetworkauth/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtnetworkauth/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtnetworkauth/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtnetworkauth/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtnetworkauth/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtnetworkauth/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtnetworkauth/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtnetworkauth/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtnetworkauth/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtnetworkauth/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtnetworkauth/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtnetworkauth/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtnetworkauth/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtnetworkauth/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtnetworkauth/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtnetworkauth/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtnetworkauth/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtnetworkauth/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtnetworkauth/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtnetworkauth/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtnetworkauth/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtnetworkauth/.git/hooks/post-commit ...
qtnetworkauth/.git/hooks/post-commit: Assembler messages:
qtnetworkauth/.git/hooks/post-commit: Warning: end of file in comment
qtnetworkauth/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtnetworkauth/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtnetworkauth/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtpurchasing/.git/hooks/commit-msg ...
qtpurchasing/.git/hooks/commit-msg: Assembler messages:
qtpurchasing/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtpurchasing/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtpurchasing/.git/hooks/commit-msg:29: Error: bad expression
qtpurchasing/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtpurchasing/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtpurchasing/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtpurchasing/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtpurchasing/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtpurchasing/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtpurchasing/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtpurchasing/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtpurchasing/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtpurchasing/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtpurchasing/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtpurchasing/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtpurchasing/.git/hooks/commit-msg:47: Error: bad expression
qtpurchasing/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtpurchasing/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtpurchasing/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtpurchasing/.git/hooks/commit-msg:52: Error: bad expression
qtpurchasing/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtpurchasing/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtpurchasing/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtpurchasing/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtpurchasing/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtpurchasing/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtpurchasing/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtpurchasing/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtpurchasing/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtpurchasing/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtpurchasing/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtpurchasing/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtpurchasing/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtpurchasing/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtpurchasing/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtpurchasing/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtpurchasing/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtpurchasing/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtpurchasing/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtpurchasing/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtpurchasing/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtpurchasing/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtpurchasing/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtpurchasing/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtpurchasing/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtpurchasing/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtpurchasing/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtpurchasing/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtpurchasing/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtpurchasing/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtpurchasing/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtpurchasing/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtpurchasing/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtpurchasing/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtpurchasing/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtpurchasing/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtpurchasing/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtpurchasing/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtpurchasing/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtpurchasing/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtpurchasing/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtpurchasing/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtpurchasing/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtpurchasing/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtpurchasing/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtpurchasing/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtpurchasing/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtpurchasing/.git/hooks/post-commit ...
qtpurchasing/.git/hooks/post-commit: Assembler messages:
qtpurchasing/.git/hooks/post-commit: Warning: end of file in comment
qtpurchasing/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtpurchasing/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtpurchasing/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtqa/.git/hooks/commit-msg ...
qtqa/.git/hooks/commit-msg: Assembler messages:
qtqa/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtqa/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtqa/.git/hooks/commit-msg:29: Error: bad expression
qtqa/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtqa/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtqa/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtqa/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtqa/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtqa/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtqa/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtqa/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtqa/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtqa/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtqa/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtqa/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtqa/.git/hooks/commit-msg:47: Error: bad expression
qtqa/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtqa/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtqa/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtqa/.git/hooks/commit-msg:52: Error: bad expression
qtqa/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtqa/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtqa/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtqa/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtqa/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtqa/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtqa/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtqa/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtqa/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtqa/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtqa/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtqa/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtqa/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtqa/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtqa/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtqa/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtqa/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtqa/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtqa/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtqa/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtqa/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtqa/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtqa/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtqa/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtqa/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtqa/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtqa/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtqa/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtqa/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtqa/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtqa/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtqa/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtqa/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtqa/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtqa/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtqa/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtqa/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtqa/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtqa/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtqa/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtqa/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtqa/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtqa/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtqa/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtqa/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtqa/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtqa/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtqa/.git/hooks/post-commit ...
qtqa/.git/hooks/post-commit: Assembler messages:
qtqa/.git/hooks/post-commit: Warning: end of file in comment
qtqa/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtqa/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtqa/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtquick3d/.git/hooks/commit-msg ...
qtquick3d/.git/hooks/commit-msg: Assembler messages:
qtquick3d/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtquick3d/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtquick3d/.git/hooks/commit-msg:29: Error: bad expression
qtquick3d/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtquick3d/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtquick3d/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtquick3d/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtquick3d/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtquick3d/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtquick3d/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtquick3d/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtquick3d/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtquick3d/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtquick3d/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtquick3d/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtquick3d/.git/hooks/commit-msg:47: Error: bad expression
qtquick3d/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtquick3d/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtquick3d/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtquick3d/.git/hooks/commit-msg:52: Error: bad expression
qtquick3d/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtquick3d/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtquick3d/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtquick3d/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtquick3d/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtquick3d/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtquick3d/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtquick3d/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtquick3d/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtquick3d/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtquick3d/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtquick3d/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtquick3d/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtquick3d/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtquick3d/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtquick3d/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtquick3d/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtquick3d/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtquick3d/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtquick3d/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtquick3d/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtquick3d/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtquick3d/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtquick3d/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtquick3d/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtquick3d/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtquick3d/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtquick3d/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtquick3d/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtquick3d/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtquick3d/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtquick3d/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtquick3d/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtquick3d/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtquick3d/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtquick3d/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtquick3d/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtquick3d/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtquick3d/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtquick3d/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtquick3d/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtquick3d/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtquick3d/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtquick3d/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtquick3d/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtquick3d/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtquick3d/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtquick3d/.git/hooks/post-commit ...
qtquick3d/.git/hooks/post-commit: Assembler messages:
qtquick3d/.git/hooks/post-commit: Warning: end of file in comment
qtquick3d/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtquick3d/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtquick3d/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtquickcontrols/.git/hooks/commit-msg ...
qtquickcontrols/.git/hooks/commit-msg: Assembler messages:
qtquickcontrols/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtquickcontrols/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtquickcontrols/.git/hooks/commit-msg:29: Error: bad expression
qtquickcontrols/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtquickcontrols/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtquickcontrols/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtquickcontrols/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtquickcontrols/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtquickcontrols/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtquickcontrols/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtquickcontrols/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtquickcontrols/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtquickcontrols/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtquickcontrols/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtquickcontrols/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtquickcontrols/.git/hooks/commit-msg:47: Error: bad expression
qtquickcontrols/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtquickcontrols/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtquickcontrols/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtquickcontrols/.git/hooks/commit-msg:52: Error: bad expression
qtquickcontrols/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtquickcontrols/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtquickcontrols/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtquickcontrols/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtquickcontrols/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtquickcontrols/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtquickcontrols/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtquickcontrols/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtquickcontrols/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtquickcontrols/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtquickcontrols/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtquickcontrols/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtquickcontrols/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtquickcontrols/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtquickcontrols/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtquickcontrols/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtquickcontrols/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtquickcontrols/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtquickcontrols/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtquickcontrols/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtquickcontrols/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtquickcontrols/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtquickcontrols/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtquickcontrols/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtquickcontrols/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtquickcontrols/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtquickcontrols/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtquickcontrols/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtquickcontrols/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtquickcontrols/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtquickcontrols/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtquickcontrols/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtquickcontrols/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtquickcontrols/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtquickcontrols/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtquickcontrols/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtquickcontrols/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtquickcontrols/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtquickcontrols/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtquickcontrols/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtquickcontrols/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtquickcontrols/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtquickcontrols/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtquickcontrols/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtquickcontrols/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtquickcontrols/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtquickcontrols/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtquickcontrols/.git/hooks/post-commit ...
qtquickcontrols/.git/hooks/post-commit: Assembler messages:
qtquickcontrols/.git/hooks/post-commit: Warning: end of file in comment
qtquickcontrols/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtquickcontrols/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtquickcontrols/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtquickcontrols2/.git/hooks/commit-msg ...
qtquickcontrols2/.git/hooks/commit-msg: Assembler messages:
qtquickcontrols2/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtquickcontrols2/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtquickcontrols2/.git/hooks/commit-msg:29: Error: bad expression
qtquickcontrols2/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtquickcontrols2/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtquickcontrols2/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtquickcontrols2/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtquickcontrols2/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtquickcontrols2/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtquickcontrols2/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtquickcontrols2/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtquickcontrols2/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtquickcontrols2/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtquickcontrols2/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtquickcontrols2/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtquickcontrols2/.git/hooks/commit-msg:47: Error: bad expression
qtquickcontrols2/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtquickcontrols2/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtquickcontrols2/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtquickcontrols2/.git/hooks/commit-msg:52: Error: bad expression
qtquickcontrols2/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtquickcontrols2/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtquickcontrols2/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtquickcontrols2/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtquickcontrols2/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtquickcontrols2/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtquickcontrols2/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtquickcontrols2/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtquickcontrols2/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtquickcontrols2/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtquickcontrols2/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtquickcontrols2/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtquickcontrols2/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtquickcontrols2/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtquickcontrols2/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtquickcontrols2/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtquickcontrols2/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtquickcontrols2/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtquickcontrols2/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtquickcontrols2/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtquickcontrols2/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtquickcontrols2/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtquickcontrols2/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtquickcontrols2/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtquickcontrols2/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtquickcontrols2/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtquickcontrols2/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtquickcontrols2/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtquickcontrols2/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtquickcontrols2/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtquickcontrols2/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtquickcontrols2/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtquickcontrols2/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtquickcontrols2/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtquickcontrols2/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtquickcontrols2/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtquickcontrols2/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtquickcontrols2/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtquickcontrols2/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtquickcontrols2/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtquickcontrols2/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtquickcontrols2/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtquickcontrols2/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtquickcontrols2/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtquickcontrols2/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtquickcontrols2/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtquickcontrols2/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtquickcontrols2/.git/hooks/post-commit ...
qtquickcontrols2/.git/hooks/post-commit: Assembler messages:
qtquickcontrols2/.git/hooks/post-commit: Warning: end of file in comment
qtquickcontrols2/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtquickcontrols2/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtquickcontrols2/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtquicktimeline/.git/hooks/commit-msg ...
qtquicktimeline/.git/hooks/commit-msg: Assembler messages:
qtquicktimeline/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtquicktimeline/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtquicktimeline/.git/hooks/commit-msg:29: Error: bad expression
qtquicktimeline/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtquicktimeline/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtquicktimeline/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtquicktimeline/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtquicktimeline/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtquicktimeline/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtquicktimeline/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtquicktimeline/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtquicktimeline/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtquicktimeline/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtquicktimeline/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtquicktimeline/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtquicktimeline/.git/hooks/commit-msg:47: Error: bad expression
qtquicktimeline/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtquicktimeline/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtquicktimeline/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtquicktimeline/.git/hooks/commit-msg:52: Error: bad expression
qtquicktimeline/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtquicktimeline/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtquicktimeline/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtquicktimeline/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtquicktimeline/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtquicktimeline/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtquicktimeline/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtquicktimeline/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtquicktimeline/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtquicktimeline/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtquicktimeline/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtquicktimeline/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtquicktimeline/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtquicktimeline/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtquicktimeline/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtquicktimeline/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtquicktimeline/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtquicktimeline/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtquicktimeline/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtquicktimeline/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtquicktimeline/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtquicktimeline/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtquicktimeline/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtquicktimeline/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtquicktimeline/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtquicktimeline/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtquicktimeline/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtquicktimeline/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtquicktimeline/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtquicktimeline/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtquicktimeline/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtquicktimeline/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtquicktimeline/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtquicktimeline/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtquicktimeline/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtquicktimeline/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtquicktimeline/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtquicktimeline/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtquicktimeline/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtquicktimeline/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtquicktimeline/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtquicktimeline/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtquicktimeline/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtquicktimeline/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtquicktimeline/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtquicktimeline/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtquicktimeline/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtquicktimeline/.git/hooks/post-commit ...
qtquicktimeline/.git/hooks/post-commit: Assembler messages:
qtquicktimeline/.git/hooks/post-commit: Warning: end of file in comment
qtquicktimeline/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtquicktimeline/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtquicktimeline/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtremoteobjects/.git/hooks/commit-msg ...
qtremoteobjects/.git/hooks/commit-msg: Assembler messages:
qtremoteobjects/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtremoteobjects/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtremoteobjects/.git/hooks/commit-msg:29: Error: bad expression
qtremoteobjects/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtremoteobjects/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtremoteobjects/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtremoteobjects/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtremoteobjects/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtremoteobjects/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtremoteobjects/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtremoteobjects/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtremoteobjects/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtremoteobjects/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtremoteobjects/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtremoteobjects/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtremoteobjects/.git/hooks/commit-msg:47: Error: bad expression
qtremoteobjects/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtremoteobjects/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtremoteobjects/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtremoteobjects/.git/hooks/commit-msg:52: Error: bad expression
qtremoteobjects/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtremoteobjects/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtremoteobjects/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtremoteobjects/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtremoteobjects/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtremoteobjects/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtremoteobjects/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtremoteobjects/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtremoteobjects/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtremoteobjects/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtremoteobjects/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtremoteobjects/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtremoteobjects/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtremoteobjects/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtremoteobjects/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtremoteobjects/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtremoteobjects/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtremoteobjects/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtremoteobjects/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtremoteobjects/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtremoteobjects/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtremoteobjects/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtremoteobjects/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtremoteobjects/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtremoteobjects/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtremoteobjects/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtremoteobjects/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtremoteobjects/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtremoteobjects/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtremoteobjects/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtremoteobjects/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtremoteobjects/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtremoteobjects/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtremoteobjects/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtremoteobjects/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtremoteobjects/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtremoteobjects/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtremoteobjects/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtremoteobjects/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtremoteobjects/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtremoteobjects/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtremoteobjects/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtremoteobjects/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtremoteobjects/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtremoteobjects/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtremoteobjects/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtremoteobjects/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtremoteobjects/.git/hooks/post-commit ...
qtremoteobjects/.git/hooks/post-commit: Assembler messages:
qtremoteobjects/.git/hooks/post-commit: Warning: end of file in comment
qtremoteobjects/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtremoteobjects/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtremoteobjects/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtrepotools/.git/hooks/commit-msg ...
qtrepotools/.git/hooks/commit-msg: Assembler messages:
qtrepotools/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtrepotools/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtrepotools/.git/hooks/commit-msg:29: Error: bad expression
qtrepotools/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtrepotools/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtrepotools/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtrepotools/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtrepotools/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtrepotools/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtrepotools/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtrepotools/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtrepotools/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtrepotools/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtrepotools/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtrepotools/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtrepotools/.git/hooks/commit-msg:47: Error: bad expression
qtrepotools/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtrepotools/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtrepotools/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtrepotools/.git/hooks/commit-msg:52: Error: bad expression
qtrepotools/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtrepotools/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtrepotools/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtrepotools/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtrepotools/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtrepotools/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtrepotools/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtrepotools/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtrepotools/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtrepotools/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtrepotools/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtrepotools/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtrepotools/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtrepotools/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtrepotools/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtrepotools/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtrepotools/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtrepotools/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtrepotools/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtrepotools/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtrepotools/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtrepotools/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtrepotools/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtrepotools/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtrepotools/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtrepotools/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtrepotools/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtrepotools/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtrepotools/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtrepotools/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtrepotools/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtrepotools/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtrepotools/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtrepotools/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtrepotools/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtrepotools/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtrepotools/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtrepotools/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtrepotools/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtrepotools/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtrepotools/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtrepotools/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtrepotools/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtrepotools/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtrepotools/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtrepotools/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtrepotools/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtrepotools/.git/hooks/post-commit ...
qtrepotools/.git/hooks/post-commit: Assembler messages:
qtrepotools/.git/hooks/post-commit: Warning: end of file in comment
qtrepotools/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtrepotools/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtrepotools/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtscript/.git/hooks/commit-msg ...
qtscript/.git/hooks/commit-msg: Assembler messages:
qtscript/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtscript/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtscript/.git/hooks/commit-msg:29: Error: bad expression
qtscript/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtscript/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtscript/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtscript/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtscript/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtscript/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtscript/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtscript/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtscript/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtscript/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtscript/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtscript/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtscript/.git/hooks/commit-msg:47: Error: bad expression
qtscript/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtscript/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtscript/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtscript/.git/hooks/commit-msg:52: Error: bad expression
qtscript/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtscript/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtscript/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtscript/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtscript/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtscript/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtscript/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtscript/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtscript/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtscript/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtscript/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtscript/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtscript/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtscript/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtscript/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtscript/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtscript/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtscript/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtscript/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtscript/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtscript/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtscript/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtscript/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtscript/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtscript/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtscript/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtscript/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtscript/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtscript/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtscript/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtscript/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtscript/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtscript/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtscript/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtscript/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtscript/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtscript/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtscript/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtscript/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtscript/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtscript/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtscript/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtscript/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtscript/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtscript/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtscript/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtscript/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtscript/.git/hooks/post-commit ...
qtscript/.git/hooks/post-commit: Assembler messages:
qtscript/.git/hooks/post-commit: Warning: end of file in comment
qtscript/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtscript/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtscript/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtscxml/.git/hooks/commit-msg ...
qtscxml/.git/hooks/commit-msg: Assembler messages:
qtscxml/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtscxml/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtscxml/.git/hooks/commit-msg:29: Error: bad expression
qtscxml/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtscxml/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtscxml/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtscxml/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtscxml/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtscxml/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtscxml/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtscxml/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtscxml/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtscxml/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtscxml/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtscxml/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtscxml/.git/hooks/commit-msg:47: Error: bad expression
qtscxml/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtscxml/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtscxml/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtscxml/.git/hooks/commit-msg:52: Error: bad expression
qtscxml/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtscxml/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtscxml/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtscxml/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtscxml/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtscxml/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtscxml/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtscxml/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtscxml/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtscxml/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtscxml/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtscxml/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtscxml/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtscxml/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtscxml/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtscxml/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtscxml/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtscxml/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtscxml/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtscxml/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtscxml/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtscxml/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtscxml/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtscxml/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtscxml/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtscxml/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtscxml/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtscxml/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtscxml/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtscxml/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtscxml/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtscxml/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtscxml/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtscxml/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtscxml/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtscxml/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtscxml/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtscxml/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtscxml/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtscxml/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtscxml/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtscxml/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtscxml/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtscxml/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtscxml/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtscxml/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtscxml/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtscxml/.git/hooks/post-commit ...
qtscxml/.git/hooks/post-commit: Assembler messages:
qtscxml/.git/hooks/post-commit: Warning: end of file in comment
qtscxml/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtscxml/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtscxml/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtsensors/.git/hooks/commit-msg ...
qtsensors/.git/hooks/commit-msg: Assembler messages:
qtsensors/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtsensors/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtsensors/.git/hooks/commit-msg:29: Error: bad expression
qtsensors/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtsensors/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtsensors/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtsensors/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtsensors/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtsensors/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtsensors/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtsensors/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtsensors/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtsensors/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtsensors/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtsensors/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtsensors/.git/hooks/commit-msg:47: Error: bad expression
qtsensors/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtsensors/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtsensors/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtsensors/.git/hooks/commit-msg:52: Error: bad expression
qtsensors/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtsensors/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtsensors/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtsensors/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtsensors/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtsensors/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtsensors/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtsensors/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtsensors/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtsensors/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtsensors/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtsensors/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtsensors/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtsensors/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtsensors/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtsensors/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtsensors/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtsensors/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtsensors/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtsensors/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtsensors/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtsensors/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtsensors/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtsensors/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtsensors/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtsensors/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtsensors/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtsensors/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtsensors/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtsensors/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtsensors/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtsensors/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtsensors/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtsensors/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtsensors/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtsensors/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtsensors/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtsensors/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtsensors/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtsensors/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtsensors/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtsensors/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtsensors/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtsensors/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtsensors/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtsensors/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtsensors/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtsensors/.git/hooks/post-commit ...
qtsensors/.git/hooks/post-commit: Assembler messages:
qtsensors/.git/hooks/post-commit: Warning: end of file in comment
qtsensors/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtsensors/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtsensors/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtserialbus/.git/hooks/commit-msg ...
qtserialbus/.git/hooks/commit-msg: Assembler messages:
qtserialbus/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtserialbus/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtserialbus/.git/hooks/commit-msg:29: Error: bad expression
qtserialbus/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtserialbus/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtserialbus/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtserialbus/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtserialbus/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtserialbus/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtserialbus/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtserialbus/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtserialbus/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtserialbus/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtserialbus/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtserialbus/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtserialbus/.git/hooks/commit-msg:47: Error: bad expression
qtserialbus/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtserialbus/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtserialbus/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtserialbus/.git/hooks/commit-msg:52: Error: bad expression
qtserialbus/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtserialbus/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtserialbus/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtserialbus/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtserialbus/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtserialbus/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtserialbus/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtserialbus/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtserialbus/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtserialbus/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtserialbus/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtserialbus/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtserialbus/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtserialbus/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtserialbus/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtserialbus/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtserialbus/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtserialbus/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtserialbus/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtserialbus/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtserialbus/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtserialbus/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtserialbus/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtserialbus/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtserialbus/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtserialbus/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtserialbus/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtserialbus/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtserialbus/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtserialbus/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtserialbus/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtserialbus/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtserialbus/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtserialbus/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtserialbus/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtserialbus/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtserialbus/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtserialbus/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtserialbus/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtserialbus/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtserialbus/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtserialbus/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtserialbus/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtserialbus/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtserialbus/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtserialbus/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtserialbus/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtserialbus/.git/hooks/post-commit ...
qtserialbus/.git/hooks/post-commit: Assembler messages:
qtserialbus/.git/hooks/post-commit: Warning: end of file in comment
qtserialbus/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtserialbus/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtserialbus/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtserialport/.git/hooks/commit-msg ...
qtserialport/.git/hooks/commit-msg: Assembler messages:
qtserialport/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtserialport/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtserialport/.git/hooks/commit-msg:29: Error: bad expression
qtserialport/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtserialport/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtserialport/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtserialport/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtserialport/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtserialport/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtserialport/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtserialport/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtserialport/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtserialport/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtserialport/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtserialport/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtserialport/.git/hooks/commit-msg:47: Error: bad expression
qtserialport/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtserialport/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtserialport/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtserialport/.git/hooks/commit-msg:52: Error: bad expression
qtserialport/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtserialport/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtserialport/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtserialport/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtserialport/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtserialport/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtserialport/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtserialport/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtserialport/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtserialport/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtserialport/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtserialport/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtserialport/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtserialport/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtserialport/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtserialport/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtserialport/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtserialport/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtserialport/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtserialport/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtserialport/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtserialport/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtserialport/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtserialport/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtserialport/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtserialport/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtserialport/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtserialport/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtserialport/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtserialport/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtserialport/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtserialport/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtserialport/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtserialport/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtserialport/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtserialport/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtserialport/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtserialport/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtserialport/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtserialport/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtserialport/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtserialport/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtserialport/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtserialport/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtserialport/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtserialport/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtserialport/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtserialport/.git/hooks/post-commit ...
qtserialport/.git/hooks/post-commit: Assembler messages:
qtserialport/.git/hooks/post-commit: Warning: end of file in comment
qtserialport/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtserialport/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtserialport/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtspeech/.git/hooks/commit-msg ...
qtspeech/.git/hooks/commit-msg: Assembler messages:
qtspeech/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtspeech/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtspeech/.git/hooks/commit-msg:29: Error: bad expression
qtspeech/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtspeech/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtspeech/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtspeech/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtspeech/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtspeech/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtspeech/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtspeech/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtspeech/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtspeech/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtspeech/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtspeech/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtspeech/.git/hooks/commit-msg:47: Error: bad expression
qtspeech/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtspeech/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtspeech/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtspeech/.git/hooks/commit-msg:52: Error: bad expression
qtspeech/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtspeech/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtspeech/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtspeech/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtspeech/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtspeech/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtspeech/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtspeech/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtspeech/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtspeech/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtspeech/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtspeech/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtspeech/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtspeech/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtspeech/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtspeech/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtspeech/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtspeech/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtspeech/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtspeech/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtspeech/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtspeech/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtspeech/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtspeech/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtspeech/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtspeech/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtspeech/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtspeech/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtspeech/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtspeech/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtspeech/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtspeech/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtspeech/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtspeech/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtspeech/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtspeech/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtspeech/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtspeech/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtspeech/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtspeech/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtspeech/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtspeech/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtspeech/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtspeech/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtspeech/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtspeech/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtspeech/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtspeech/.git/hooks/post-commit ...
qtspeech/.git/hooks/post-commit: Assembler messages:
qtspeech/.git/hooks/post-commit: Warning: end of file in comment
qtspeech/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtspeech/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtspeech/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtsvg/.git/hooks/commit-msg ...
qtsvg/.git/hooks/commit-msg: Assembler messages:
qtsvg/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtsvg/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtsvg/.git/hooks/commit-msg:29: Error: bad expression
qtsvg/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtsvg/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtsvg/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtsvg/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtsvg/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtsvg/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtsvg/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtsvg/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtsvg/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtsvg/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtsvg/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtsvg/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtsvg/.git/hooks/commit-msg:47: Error: bad expression
qtsvg/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtsvg/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtsvg/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtsvg/.git/hooks/commit-msg:52: Error: bad expression
qtsvg/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtsvg/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtsvg/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtsvg/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtsvg/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtsvg/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtsvg/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtsvg/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtsvg/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtsvg/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtsvg/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtsvg/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtsvg/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtsvg/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtsvg/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtsvg/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtsvg/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtsvg/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtsvg/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtsvg/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtsvg/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtsvg/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtsvg/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtsvg/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtsvg/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtsvg/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtsvg/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtsvg/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtsvg/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtsvg/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtsvg/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtsvg/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtsvg/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtsvg/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtsvg/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtsvg/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtsvg/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtsvg/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtsvg/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtsvg/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtsvg/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtsvg/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtsvg/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtsvg/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtsvg/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtsvg/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtsvg/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtsvg/.git/hooks/post-commit ...
qtsvg/.git/hooks/post-commit: Assembler messages:
qtsvg/.git/hooks/post-commit: Warning: end of file in comment
qtsvg/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtsvg/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtsvg/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qttools/.git/hooks/commit-msg ...
qttools/.git/hooks/commit-msg: Assembler messages:
qttools/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qttools/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qttools/.git/hooks/commit-msg:29: Error: bad expression
qttools/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qttools/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qttools/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qttools/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qttools/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qttools/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qttools/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qttools/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qttools/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qttools/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qttools/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qttools/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qttools/.git/hooks/commit-msg:47: Error: bad expression
qttools/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qttools/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qttools/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qttools/.git/hooks/commit-msg:52: Error: bad expression
qttools/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qttools/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qttools/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qttools/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qttools/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qttools/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qttools/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qttools/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qttools/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qttools/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qttools/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qttools/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qttools/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qttools/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qttools/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qttools/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qttools/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qttools/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qttools/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qttools/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qttools/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qttools/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qttools/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qttools/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qttools/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qttools/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qttools/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qttools/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qttools/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qttools/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qttools/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qttools/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qttools/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qttools/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qttools/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qttools/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qttools/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qttools/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qttools/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qttools/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qttools/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qttools/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qttools/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qttools/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qttools/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qttools/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qttools/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qttools/.git/hooks/post-commit ...
qttools/.git/hooks/post-commit: Assembler messages:
qttools/.git/hooks/post-commit: Warning: end of file in comment
qttools/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qttools/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qttools/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qttranslations/.git/hooks/commit-msg ...
qttranslations/.git/hooks/commit-msg: Assembler messages:
qttranslations/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qttranslations/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qttranslations/.git/hooks/commit-msg:29: Error: bad expression
qttranslations/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qttranslations/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qttranslations/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qttranslations/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qttranslations/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qttranslations/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qttranslations/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qttranslations/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qttranslations/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qttranslations/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qttranslations/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qttranslations/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qttranslations/.git/hooks/commit-msg:47: Error: bad expression
qttranslations/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qttranslations/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qttranslations/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qttranslations/.git/hooks/commit-msg:52: Error: bad expression
qttranslations/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qttranslations/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qttranslations/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qttranslations/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qttranslations/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qttranslations/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qttranslations/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qttranslations/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qttranslations/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qttranslations/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qttranslations/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qttranslations/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qttranslations/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qttranslations/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qttranslations/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qttranslations/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qttranslations/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qttranslations/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qttranslations/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qttranslations/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qttranslations/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qttranslations/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qttranslations/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qttranslations/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qttranslations/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qttranslations/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qttranslations/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qttranslations/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qttranslations/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qttranslations/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qttranslations/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qttranslations/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qttranslations/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qttranslations/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qttranslations/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qttranslations/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qttranslations/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qttranslations/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qttranslations/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qttranslations/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qttranslations/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qttranslations/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qttranslations/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qttranslations/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qttranslations/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qttranslations/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qttranslations/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qttranslations/.git/hooks/post-commit ...
qttranslations/.git/hooks/post-commit: Assembler messages:
qttranslations/.git/hooks/post-commit: Warning: end of file in comment
qttranslations/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qttranslations/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qttranslations/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtvirtualkeyboard/.git/hooks/commit-msg ...
qtvirtualkeyboard/.git/hooks/commit-msg: Assembler messages:
qtvirtualkeyboard/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtvirtualkeyboard/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtvirtualkeyboard/.git/hooks/commit-msg:29: Error: bad expression
qtvirtualkeyboard/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtvirtualkeyboard/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtvirtualkeyboard/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtvirtualkeyboard/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtvirtualkeyboard/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtvirtualkeyboard/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtvirtualkeyboard/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtvirtualkeyboard/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtvirtualkeyboard/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtvirtualkeyboard/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtvirtualkeyboard/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtvirtualkeyboard/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtvirtualkeyboard/.git/hooks/commit-msg:47: Error: bad expression
qtvirtualkeyboard/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtvirtualkeyboard/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtvirtualkeyboard/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtvirtualkeyboard/.git/hooks/commit-msg:52: Error: bad expression
qtvirtualkeyboard/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtvirtualkeyboard/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtvirtualkeyboard/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtvirtualkeyboard/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtvirtualkeyboard/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtvirtualkeyboard/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtvirtualkeyboard/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtvirtualkeyboard/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtvirtualkeyboard/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtvirtualkeyboard/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtvirtualkeyboard/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtvirtualkeyboard/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtvirtualkeyboard/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtvirtualkeyboard/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtvirtualkeyboard/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtvirtualkeyboard/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtvirtualkeyboard/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtvirtualkeyboard/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtvirtualkeyboard/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtvirtualkeyboard/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtvirtualkeyboard/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtvirtualkeyboard/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtvirtualkeyboard/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtvirtualkeyboard/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtvirtualkeyboard/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtvirtualkeyboard/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtvirtualkeyboard/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtvirtualkeyboard/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtvirtualkeyboard/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtvirtualkeyboard/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtvirtualkeyboard/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtvirtualkeyboard/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtvirtualkeyboard/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtvirtualkeyboard/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtvirtualkeyboard/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtvirtualkeyboard/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtvirtualkeyboard/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtvirtualkeyboard/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtvirtualkeyboard/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtvirtualkeyboard/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtvirtualkeyboard/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtvirtualkeyboard/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtvirtualkeyboard/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtvirtualkeyboard/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtvirtualkeyboard/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtvirtualkeyboard/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtvirtualkeyboard/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtvirtualkeyboard/.git/hooks/post-commit ...
qtvirtualkeyboard/.git/hooks/post-commit: Assembler messages:
qtvirtualkeyboard/.git/hooks/post-commit: Warning: end of file in comment
qtvirtualkeyboard/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtvirtualkeyboard/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtvirtualkeyboard/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwayland/.git/hooks/commit-msg ...
qtwayland/.git/hooks/commit-msg: Assembler messages:
qtwayland/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtwayland/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtwayland/.git/hooks/commit-msg:29: Error: bad expression
qtwayland/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtwayland/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtwayland/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtwayland/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtwayland/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtwayland/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtwayland/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtwayland/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtwayland/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtwayland/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtwayland/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtwayland/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtwayland/.git/hooks/commit-msg:47: Error: bad expression
qtwayland/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtwayland/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtwayland/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtwayland/.git/hooks/commit-msg:52: Error: bad expression
qtwayland/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtwayland/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtwayland/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtwayland/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtwayland/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtwayland/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtwayland/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtwayland/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtwayland/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtwayland/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtwayland/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtwayland/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtwayland/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtwayland/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtwayland/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtwayland/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtwayland/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtwayland/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtwayland/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtwayland/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtwayland/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtwayland/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtwayland/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtwayland/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtwayland/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtwayland/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtwayland/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtwayland/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtwayland/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwayland/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtwayland/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtwayland/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwayland/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtwayland/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtwayland/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtwayland/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtwayland/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtwayland/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtwayland/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtwayland/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtwayland/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtwayland/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtwayland/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtwayland/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtwayland/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtwayland/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtwayland/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwayland/.git/hooks/post-commit ...
qtwayland/.git/hooks/post-commit: Assembler messages:
qtwayland/.git/hooks/post-commit: Warning: end of file in comment
qtwayland/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtwayland/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtwayland/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwebchannel/.git/hooks/commit-msg ...
qtwebchannel/.git/hooks/commit-msg: Assembler messages:
qtwebchannel/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtwebchannel/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtwebchannel/.git/hooks/commit-msg:29: Error: bad expression
qtwebchannel/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtwebchannel/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtwebchannel/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtwebchannel/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtwebchannel/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtwebchannel/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtwebchannel/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtwebchannel/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtwebchannel/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtwebchannel/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtwebchannel/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtwebchannel/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtwebchannel/.git/hooks/commit-msg:47: Error: bad expression
qtwebchannel/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtwebchannel/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtwebchannel/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtwebchannel/.git/hooks/commit-msg:52: Error: bad expression
qtwebchannel/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtwebchannel/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtwebchannel/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtwebchannel/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtwebchannel/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtwebchannel/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtwebchannel/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtwebchannel/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtwebchannel/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtwebchannel/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtwebchannel/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtwebchannel/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtwebchannel/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtwebchannel/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtwebchannel/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtwebchannel/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtwebchannel/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtwebchannel/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtwebchannel/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtwebchannel/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtwebchannel/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtwebchannel/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtwebchannel/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtwebchannel/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtwebchannel/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtwebchannel/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtwebchannel/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtwebchannel/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtwebchannel/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwebchannel/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtwebchannel/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtwebchannel/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwebchannel/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtwebchannel/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtwebchannel/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtwebchannel/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtwebchannel/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtwebchannel/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtwebchannel/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtwebchannel/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtwebchannel/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtwebchannel/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtwebchannel/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtwebchannel/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtwebchannel/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtwebchannel/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtwebchannel/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwebchannel/.git/hooks/post-commit ...
qtwebchannel/.git/hooks/post-commit: Assembler messages:
qtwebchannel/.git/hooks/post-commit: Warning: end of file in comment
qtwebchannel/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtwebchannel/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtwebchannel/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwebengine/.git/hooks/commit-msg ...
qtwebengine/.git/hooks/commit-msg: Assembler messages:
qtwebengine/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtwebengine/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtwebengine/.git/hooks/commit-msg:29: Error: bad expression
qtwebengine/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtwebengine/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtwebengine/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtwebengine/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtwebengine/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtwebengine/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtwebengine/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtwebengine/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtwebengine/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtwebengine/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtwebengine/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtwebengine/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtwebengine/.git/hooks/commit-msg:47: Error: bad expression
qtwebengine/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtwebengine/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtwebengine/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtwebengine/.git/hooks/commit-msg:52: Error: bad expression
qtwebengine/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtwebengine/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtwebengine/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtwebengine/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtwebengine/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtwebengine/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtwebengine/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtwebengine/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtwebengine/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtwebengine/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtwebengine/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtwebengine/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtwebengine/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtwebengine/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtwebengine/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtwebengine/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtwebengine/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtwebengine/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtwebengine/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtwebengine/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtwebengine/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtwebengine/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtwebengine/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtwebengine/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtwebengine/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtwebengine/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtwebengine/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtwebengine/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtwebengine/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwebengine/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtwebengine/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtwebengine/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwebengine/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtwebengine/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtwebengine/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtwebengine/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtwebengine/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtwebengine/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtwebengine/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtwebengine/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtwebengine/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtwebengine/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtwebengine/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtwebengine/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtwebengine/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtwebengine/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtwebengine/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwebengine/.git/hooks/post-commit ...
qtwebengine/.git/hooks/post-commit: Assembler messages:
qtwebengine/.git/hooks/post-commit: Warning: end of file in comment
qtwebengine/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtwebengine/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtwebengine/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwebglplugin/.git/hooks/commit-msg ...
qtwebglplugin/.git/hooks/commit-msg: Assembler messages:
qtwebglplugin/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtwebglplugin/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtwebglplugin/.git/hooks/commit-msg:29: Error: bad expression
qtwebglplugin/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtwebglplugin/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtwebglplugin/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtwebglplugin/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtwebglplugin/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtwebglplugin/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtwebglplugin/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtwebglplugin/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtwebglplugin/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtwebglplugin/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtwebglplugin/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtwebglplugin/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtwebglplugin/.git/hooks/commit-msg:47: Error: bad expression
qtwebglplugin/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtwebglplugin/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtwebglplugin/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtwebglplugin/.git/hooks/commit-msg:52: Error: bad expression
qtwebglplugin/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtwebglplugin/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtwebglplugin/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtwebglplugin/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtwebglplugin/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtwebglplugin/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtwebglplugin/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtwebglplugin/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtwebglplugin/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtwebglplugin/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtwebglplugin/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtwebglplugin/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtwebglplugin/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtwebglplugin/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtwebglplugin/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtwebglplugin/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtwebglplugin/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtwebglplugin/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtwebglplugin/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtwebglplugin/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtwebglplugin/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtwebglplugin/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtwebglplugin/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtwebglplugin/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtwebglplugin/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtwebglplugin/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtwebglplugin/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtwebglplugin/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtwebglplugin/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwebglplugin/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtwebglplugin/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtwebglplugin/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwebglplugin/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtwebglplugin/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtwebglplugin/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtwebglplugin/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtwebglplugin/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtwebglplugin/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtwebglplugin/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtwebglplugin/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtwebglplugin/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtwebglplugin/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtwebglplugin/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtwebglplugin/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtwebglplugin/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtwebglplugin/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtwebglplugin/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwebglplugin/.git/hooks/post-commit ...
qtwebglplugin/.git/hooks/post-commit: Assembler messages:
qtwebglplugin/.git/hooks/post-commit: Warning: end of file in comment
qtwebglplugin/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtwebglplugin/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtwebglplugin/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtmultimedia/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtmultimedia/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtnetworkauth/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtnetworkauth/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtpurchasing/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtpurchasing/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtqa/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtqa/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtquick3d/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtquick3d/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtquickcontrols/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtquickcontrols/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtquickcontrols2/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtquickcontrols2/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtquicktimeline/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtquicktimeline/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtremoteobjects/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtremoteobjects/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtrepotools/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
      as qtrepotools/.git/hooks/post-commit ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
      as qtscript/.git/hooks/commit-msg ...
Aliasing /home/aiegoo/repos/projects/qt5/qtrepotooAliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwebsockets/.git/hooks/commit-msg ...
qtwebsockets/.git/hooks/commit-msg: Assembler messages:
qtwebsockets/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtwebsockets/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtwebsockets/.git/hooks/commit-msg:29: Error: bad expression
qtwebsockets/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtwebsockets/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtwebsockets/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtwebsockets/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtwebsockets/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtwebsockets/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtwebsockets/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtwebsockets/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtwebsockets/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtwebsockets/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtwebsockets/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtwebsockets/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtwebsockets/.git/hooks/commit-msg:47: Error: bad expression
qtwebsockets/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtwebsockets/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtwebsockets/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtwebsockets/.git/hooks/commit-msg:52: Error: bad expression
qtwebsockets/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtwebsockets/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtwebsockets/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtwebsockets/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtwebsockets/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtwebsockets/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtwebsockets/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtwebsockets/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtwebsockets/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtwebsockets/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtwebsockets/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtwebsockets/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtwebsockets/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtwebsockets/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtwebsockets/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtwebsockets/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtwebsockets/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtwebsockets/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtwebsockets/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtwebsockets/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtwebsockets/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtwebsockets/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtwebsockets/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtwebsockets/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtwebsockets/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtwebsockets/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtwebsockets/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtwebsockets/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtwebsockets/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwebsockets/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtwebsockets/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtwebsockets/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwebsockets/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtwebsockets/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtwebsockets/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtwebsockets/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtwebsockets/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtwebsockets/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtwebsockets/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtwebsockets/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtwebsockets/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtwebsockets/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtwebsockets/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtwebsockets/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtwebsockets/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtwebsockets/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtwebsockets/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwebsockets/.git/hooks/post-commit ...
qtwebsockets/.git/hooks/post-commit: Assembler messages:
qtwebsockets/.git/hooks/post-commit: Warning: end of file in comment
qtwebsockets/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtwebsockets/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtwebsockets/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwebview/.git/hooks/commit-msg ...
qtwebview/.git/hooks/commit-msg: Assembler messages:
qtwebview/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtwebview/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtwebview/.git/hooks/commit-msg:29: Error: bad expression
qtwebview/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtwebview/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtwebview/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtwebview/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtwebview/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtwebview/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtwebview/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtwebview/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtwebview/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtwebview/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtwebview/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtwebview/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtwebview/.git/hooks/commit-msg:47: Error: bad expression
qtwebview/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtwebview/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtwebview/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtwebview/.git/hooks/commit-msg:52: Error: bad expression
qtwebview/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtwebview/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtwebview/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtwebview/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtwebview/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtwebview/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtwebview/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtwebview/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtwebview/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtwebview/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtwebview/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtwebview/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtwebview/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtwebview/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtwebview/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtwebview/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtwebview/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtwebview/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtwebview/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtwebview/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtwebview/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtwebview/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtwebview/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtwebview/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtwebview/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtwebview/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtwebview/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtwebview/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtwebview/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwebview/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtwebview/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtwebview/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwebview/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtwebview/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtwebview/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtwebview/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtwebview/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtwebview/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtwebview/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtwebview/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtwebview/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtwebview/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtwebview/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtwebview/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtwebview/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtwebview/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtwebview/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwebview/.git/hooks/post-commit ...
qtwebview/.git/hooks/post-commit: Assembler messages:
qtwebview/.git/hooks/post-commit: Warning: end of file in comment
qtwebview/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtwebview/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtwebview/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwinextras/.git/hooks/commit-msg ...
qtwinextras/.git/hooks/commit-msg: Assembler messages:
qtwinextras/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtwinextras/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtwinextras/.git/hooks/commit-msg:29: Error: bad expression
qtwinextras/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtwinextras/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtwinextras/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtwinextras/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtwinextras/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtwinextras/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtwinextras/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtwinextras/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtwinextras/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtwinextras/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtwinextras/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtwinextras/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtwinextras/.git/hooks/commit-msg:47: Error: bad expression
qtwinextras/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtwinextras/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtwinextras/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtwinextras/.git/hooks/commit-msg:52: Error: bad expression
qtwinextras/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtwinextras/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtwinextras/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtwinextras/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtwinextras/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtwinextras/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtwinextras/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtwinextras/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtwinextras/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtwinextras/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtwinextras/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtwinextras/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtwinextras/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtwinextras/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtwinextras/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtwinextras/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtwinextras/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtwinextras/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtwinextras/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtwinextras/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtwinextras/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtwinextras/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtwinextras/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtwinextras/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtwinextras/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtwinextras/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtwinextras/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtwinextras/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtwinextras/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwinextras/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtwinextras/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtwinextras/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwinextras/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtwinextras/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtwinextras/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtwinextras/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtwinextras/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtwinextras/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtwinextras/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtwinextras/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtwinextras/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtwinextras/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtwinextras/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtwinextras/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtwinextras/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtwinextras/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtwinextras/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwinextras/.git/hooks/post-commit ...
qtwinextras/.git/hooks/post-commit: Assembler messages:
qtwinextras/.git/hooks/post-commit: Warning: end of file in comment
qtwinextras/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtwinextras/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtwinextras/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtx11extras/.git/hooks/commit-msg ...
qtx11extras/.git/hooks/commit-msg: Assembler messages:
qtx11extras/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtx11extras/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtx11extras/.git/hooks/commit-msg:29: Error: bad expression
qtx11extras/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtx11extras/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtx11extras/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtx11extras/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtx11extras/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtx11extras/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtx11extras/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtx11extras/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtx11extras/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtx11extras/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtx11extras/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtx11extras/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtx11extras/.git/hooks/commit-msg:47: Error: bad expression
qtx11extras/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtx11extras/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtx11extras/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtx11extras/.git/hooks/commit-msg:52: Error: bad expression
qtx11extras/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtx11extras/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtx11extras/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtx11extras/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtx11extras/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtx11extras/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtx11extras/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtx11extras/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtx11extras/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtx11extras/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtx11extras/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtx11extras/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtx11extras/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtx11extras/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtx11extras/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtx11extras/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtx11extras/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtx11extras/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtx11extras/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtx11extras/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtx11extras/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtx11extras/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtx11extras/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtx11extras/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtx11extras/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtx11extras/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtx11extras/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtx11extras/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtx11extras/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtx11extras/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtx11extras/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtx11extras/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtx11extras/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtx11extras/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtx11extras/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtx11extras/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtx11extras/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtx11extras/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtx11extras/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtx11extras/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtx11extras/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtx11extras/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtx11extras/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtx11extras/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtx11extras/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtx11extras/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtx11extras/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtx11extras/.git/hooks/post-commit ...
qtx11extras/.git/hooks/post-commit: Assembler messages:
qtx11extras/.git/hooks/post-commit: Warning: end of file in comment
qtx11extras/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtx11extras/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtx11extras/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtxmlpatterns/.git/hooks/commit-msg ...
qtxmlpatterns/.git/hooks/commit-msg: Assembler messages:
qtxmlpatterns/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtxmlpatterns/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtxmlpatterns/.git/hooks/commit-msg:29: Error: bad expression
qtxmlpatterns/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtxmlpatterns/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtxmlpatterns/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtxmlpatterns/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtxmlpatterns/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtxmlpatterns/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtxmlpatterns/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtxmlpatterns/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtxmlpatterns/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtxmlpatterns/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtxmlpatterns/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtxmlpatterns/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtxmlpatterns/.git/hooks/commit-msg:47: Error: bad expression
qtxmlpatterns/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtxmlpatterns/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtxmlpatterns/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtxmlpatterns/.git/hooks/commit-msg:52: Error: bad expression
qtxmlpatterns/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtxmlpatterns/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtxmlpatterns/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtxmlpatterns/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtxmlpatterns/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtxmlpatterns/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtxmlpatterns/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtxmlpatterns/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtxmlpatterns/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtxmlpatterns/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtxmlpatterns/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtxmlpatterns/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtxmlpatterns/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtxmlpatterns/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtxmlpatterns/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtxmlpatterns/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtxmlpatterns/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtxmlpatterns/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtxmlpatterns/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtxmlpatterns/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtxmlpatterns/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtxmlpatterns/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtxmlpatterns/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtxmlpatterns/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtxmlpatterns/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtxmlpatterns/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtxmlpatterns/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtxmlpatterns/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtxmlpatterns/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtxmlpatterns/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtxmlpatterns/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtxmlpatterns/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtxmlpatterns/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtxmlpatterns/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtxmlpatterns/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtxmlpatterns/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtxmlpatterns/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtxmlpatterns/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtxmlpatterns/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtxmlpatterns/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtxmlpatterns/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtxmlpatterns/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtxmlpatterns/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtxmlpatterns/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtxmlpatterns/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtxmlpatterns/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtxmlpatterns/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtxmlpatterns/.git/hooks/post-commit ...
qtxmlpatterns/.git/hooks/post-commit: Assembler messages:
qtxmlpatterns/.git/hooks/post-commit: Warning: end of file in comment
qtxmlpatterns/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtxmlpatterns/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtxmlpatterns/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtmultimedia/.git/hooks/commit-msg ...
qtmultimedia/.git/hooks/commit-msg: Assembler messages:
qtmultimedia/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtmultimedia/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtmultimedia/.git/hooks/commit-msg:29: Error: bad expression
qtmultimedia/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtmultimedia/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtmultimedia/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtmultimedia/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtmultimedia/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtmultimedia/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtmultimedia/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtmultimedia/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtmultimedia/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtmultimedia/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtmultimedia/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtmultimedia/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtmultimedia/.git/hooks/commit-msg:47: Error: bad expression
qtmultimedia/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtmultimedia/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtmultimedia/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtmultimedia/.git/hooks/commit-msg:52: Error: bad expression
qtmultimedia/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtmultimedia/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtmultimedia/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtmultimedia/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtmultimedia/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtmultimedia/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtmultimedia/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtmultimedia/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtmultimedia/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtmultimedia/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtmultimedia/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtmultimedia/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtmultimedia/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtmultimedia/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtmultimedia/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtmultimedia/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtmultimedia/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtmultimedia/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtmultimedia/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtmultimedia/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtmultimedia/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtmultimedia/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtmultimedia/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtmultimedia/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtmultimedia/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtmultimedia/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtmultimedia/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtmultimedia/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtmultimedia/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtmultimedia/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtmultimedia/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtmultimedia/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtmultimedia/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtmultimedia/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtmultimedia/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtmultimedia/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtmultimedia/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtmultimedia/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtmultimedia/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtmultimedia/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtmultimedia/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtmultimedia/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtmultimedia/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtmultimedia/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtmultimedia/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtmultimedia/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtmultimedia/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtmultimedia/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtmultimedia/.git/hooks/post-commit ...
qtmultimedia/.git/hooks/post-commit: Assembler messages:
qtmultimedia/.git/hooks/post-commit: Warning: end of file in comment
qtmultimedia/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtmultimedia/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtmultimedia/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtnetworkauth/.git/hooks/commit-msg ...
qtnetworkauth/.git/hooks/commit-msg: Assembler messages:
qtnetworkauth/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtnetworkauth/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtnetworkauth/.git/hooks/commit-msg:29: Error: bad expression
qtnetworkauth/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtnetworkauth/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtnetworkauth/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtnetworkauth/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtnetworkauth/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtnetworkauth/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtnetworkauth/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtnetworkauth/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtnetworkauth/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtnetworkauth/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtnetworkauth/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtnetworkauth/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtnetworkauth/.git/hooks/commit-msg:47: Error: bad expression
qtnetworkauth/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtnetworkauth/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtnetworkauth/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtnetworkauth/.git/hooks/commit-msg:52: Error: bad expression
qtnetworkauth/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtnetworkauth/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtnetworkauth/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtnetworkauth/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtnetworkauth/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtnetworkauth/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtnetworkauth/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtnetworkauth/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtnetworkauth/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtnetworkauth/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtnetworkauth/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtnetworkauth/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtnetworkauth/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtnetworkauth/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtnetworkauth/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtnetworkauth/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtnetworkauth/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtnetworkauth/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtnetworkauth/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtnetworkauth/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtnetworkauth/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtnetworkauth/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtnetworkauth/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtnetworkauth/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtnetworkauth/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtnetworkauth/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtnetworkauth/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtnetworkauth/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtnetworkauth/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtnetworkauth/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtnetworkauth/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtnetworkauth/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtnetworkauth/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtnetworkauth/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtnetworkauth/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtnetworkauth/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtnetworkauth/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtnetworkauth/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtnetworkauth/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtnetworkauth/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtnetworkauth/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtnetworkauth/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtnetworkauth/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtnetworkauth/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtnetworkauth/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtnetworkauth/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtnetworkauth/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtnetworkauth/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtnetworkauth/.git/hooks/post-commit ...
qtnetworkauth/.git/hooks/post-commit: Assembler messages:
qtnetworkauth/.git/hooks/post-commit: Warning: end of file in comment
qtnetworkauth/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtnetworkauth/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtnetworkauth/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtpurchasing/.git/hooks/commit-msg ...
qtpurchasing/.git/hooks/commit-msg: Assembler messages:
qtpurchasing/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtpurchasing/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtpurchasing/.git/hooks/commit-msg:29: Error: bad expression
qtpurchasing/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtpurchasing/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtpurchasing/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtpurchasing/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtpurchasing/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtpurchasing/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtpurchasing/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtpurchasing/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtpurchasing/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtpurchasing/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtpurchasing/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtpurchasing/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtpurchasing/.git/hooks/commit-msg:47: Error: bad expression
qtpurchasing/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtpurchasing/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtpurchasing/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtpurchasing/.git/hooks/commit-msg:52: Error: bad expression
qtpurchasing/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtpurchasing/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtpurchasing/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtpurchasing/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtpurchasing/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtpurchasing/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtpurchasing/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtpurchasing/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtpurchasing/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtpurchasing/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtpurchasing/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtpurchasing/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtpurchasing/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtpurchasing/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtpurchasing/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtpurchasing/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtpurchasing/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtpurchasing/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtpurchasing/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtpurchasing/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtpurchasing/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtpurchasing/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtpurchasing/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtpurchasing/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtpurchasing/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtpurchasing/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtpurchasing/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtpurchasing/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtpurchasing/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtpurchasing/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtpurchasing/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtpurchasing/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtpurchasing/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtpurchasing/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtpurchasing/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtpurchasing/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtpurchasing/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtpurchasing/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtpurchasing/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtpurchasing/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtpurchasing/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtpurchasing/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtpurchasing/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtpurchasing/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtpurchasing/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtpurchasing/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtpurchasing/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtpurchasing/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtpurchasing/.git/hooks/post-commit ...
qtpurchasing/.git/hooks/post-commit: Assembler messages:
qtpurchasing/.git/hooks/post-commit: Warning: end of file in comment
qtpurchasing/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtpurchasing/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtpurchasing/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtqa/.git/hooks/commit-msg ...
qtqa/.git/hooks/commit-msg: Assembler messages:
qtqa/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtqa/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtqa/.git/hooks/commit-msg:29: Error: bad expression
qtqa/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtqa/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtqa/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtqa/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtqa/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtqa/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtqa/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtqa/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtqa/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtqa/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtqa/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtqa/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtqa/.git/hooks/commit-msg:47: Error: bad expression
qtqa/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtqa/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtqa/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtqa/.git/hooks/commit-msg:52: Error: bad expression
qtqa/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtqa/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtqa/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtqa/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtqa/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtqa/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtqa/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtqa/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtqa/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtqa/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtqa/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtqa/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtqa/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtqa/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtqa/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtqa/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtqa/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtqa/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtqa/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtqa/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtqa/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtqa/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtqa/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtqa/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtqa/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtqa/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtqa/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtqa/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtqa/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtqa/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtqa/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtqa/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtqa/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtqa/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtqa/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtqa/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtqa/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtqa/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtqa/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtqa/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtqa/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtqa/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtqa/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtqa/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtqa/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtqa/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtqa/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtqa/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtqa/.git/hooks/post-commit ...
qtqa/.git/hooks/post-commit: Assembler messages:
qtqa/.git/hooks/post-commit: Warning: end of file in comment
qtqa/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtqa/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtqa/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtquick3d/.git/hooks/commit-msg ...
qtquick3d/.git/hooks/commit-msg: Assembler messages:
qtquick3d/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtquick3d/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtquick3d/.git/hooks/commit-msg:29: Error: bad expression
qtquick3d/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtquick3d/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtquick3d/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtquick3d/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtquick3d/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtquick3d/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtquick3d/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtquick3d/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtquick3d/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtquick3d/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtquick3d/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtquick3d/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtquick3d/.git/hooks/commit-msg:47: Error: bad expression
qtquick3d/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtquick3d/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtquick3d/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtquick3d/.git/hooks/commit-msg:52: Error: bad expression
qtquick3d/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtquick3d/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtquick3d/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtquick3d/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtquick3d/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtquick3d/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtquick3d/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtquick3d/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtquick3d/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtquick3d/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtquick3d/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtquick3d/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtquick3d/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtquick3d/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtquick3d/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtquick3d/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtquick3d/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtquick3d/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtquick3d/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtquick3d/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtquick3d/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtquick3d/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtquick3d/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtquick3d/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtquick3d/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtquick3d/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtquick3d/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtquick3d/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtquick3d/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtquick3d/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtquick3d/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtquick3d/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtquick3d/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtquick3d/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtquick3d/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtquick3d/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtquick3d/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtquick3d/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtquick3d/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtquick3d/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtquick3d/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtquick3d/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtquick3d/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtquick3d/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtquick3d/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtquick3d/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtquick3d/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtquick3d/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtquick3d/.git/hooks/post-commit ...
qtquick3d/.git/hooks/post-commit: Assembler messages:
qtquick3d/.git/hooks/post-commit: Warning: end of file in comment
qtquick3d/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtquick3d/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtquick3d/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtquickcontrols/.git/hooks/commit-msg ...
qtquickcontrols/.git/hooks/commit-msg: Assembler messages:
qtquickcontrols/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtquickcontrols/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtquickcontrols/.git/hooks/commit-msg:29: Error: bad expression
qtquickcontrols/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtquickcontrols/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtquickcontrols/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtquickcontrols/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtquickcontrols/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtquickcontrols/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtquickcontrols/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtquickcontrols/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtquickcontrols/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtquickcontrols/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtquickcontrols/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtquickcontrols/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtquickcontrols/.git/hooks/commit-msg:47: Error: bad expression
qtquickcontrols/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtquickcontrols/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtquickcontrols/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtquickcontrols/.git/hooks/commit-msg:52: Error: bad expression
qtquickcontrols/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtquickcontrols/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtquickcontrols/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtquickcontrols/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtquickcontrols/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtquickcontrols/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtquickcontrols/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtquickcontrols/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtquickcontrols/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtquickcontrols/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtquickcontrols/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtquickcontrols/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtquickcontrols/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtquickcontrols/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtquickcontrols/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtquickcontrols/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtquickcontrols/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtquickcontrols/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtquickcontrols/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtquickcontrols/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtquickcontrols/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtquickcontrols/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtquickcontrols/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtquickcontrols/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtquickcontrols/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtquickcontrols/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtquickcontrols/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtquickcontrols/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtquickcontrols/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtquickcontrols/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtquickcontrols/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtquickcontrols/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtquickcontrols/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtquickcontrols/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtquickcontrols/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtquickcontrols/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtquickcontrols/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtquickcontrols/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtquickcontrols/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtquickcontrols/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtquickcontrols/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtquickcontrols/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtquickcontrols/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtquickcontrols/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtquickcontrols/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtquickcontrols/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtquickcontrols/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtquickcontrols/.git/hooks/post-commit ...
qtquickcontrols/.git/hooks/post-commit: Assembler messages:
qtquickcontrols/.git/hooks/post-commit: Warning: end of file in comment
qtquickcontrols/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtquickcontrols/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtquickcontrols/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtquickcontrols2/.git/hooks/commit-msg ...
qtquickcontrols2/.git/hooks/commit-msg: Assembler messages:
qtquickcontrols2/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtquickcontrols2/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtquickcontrols2/.git/hooks/commit-msg:29: Error: bad expression
qtquickcontrols2/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtquickcontrols2/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtquickcontrols2/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtquickcontrols2/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtquickcontrols2/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtquickcontrols2/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtquickcontrols2/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtquickcontrols2/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtquickcontrols2/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtquickcontrols2/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtquickcontrols2/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtquickcontrols2/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtquickcontrols2/.git/hooks/commit-msg:47: Error: bad expression
qtquickcontrols2/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtquickcontrols2/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtquickcontrols2/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtquickcontrols2/.git/hooks/commit-msg:52: Error: bad expression
qtquickcontrols2/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtquickcontrols2/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtquickcontrols2/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtquickcontrols2/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtquickcontrols2/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtquickcontrols2/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtquickcontrols2/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtquickcontrols2/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtquickcontrols2/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtquickcontrols2/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtquickcontrols2/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtquickcontrols2/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtquickcontrols2/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtquickcontrols2/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtquickcontrols2/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtquickcontrols2/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtquickcontrols2/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtquickcontrols2/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtquickcontrols2/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtquickcontrols2/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtquickcontrols2/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtquickcontrols2/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtquickcontrols2/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtquickcontrols2/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtquickcontrols2/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtquickcontrols2/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtquickcontrols2/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtquickcontrols2/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtquickcontrols2/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtquickcontrols2/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtquickcontrols2/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtquickcontrols2/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtquickcontrols2/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtquickcontrols2/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtquickcontrols2/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtquickcontrols2/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtquickcontrols2/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtquickcontrols2/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtquickcontrols2/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtquickcontrols2/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtquickcontrols2/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtquickcontrols2/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtquickcontrols2/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtquickcontrols2/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtquickcontrols2/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtquickcontrols2/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtquickcontrols2/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtquickcontrols2/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtquickcontrols2/.git/hooks/post-commit ...
qtquickcontrols2/.git/hooks/post-commit: Assembler messages:
qtquickcontrols2/.git/hooks/post-commit: Warning: end of file in comment
qtquickcontrols2/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtquickcontrols2/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtquickcontrols2/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtquicktimeline/.git/hooks/commit-msg ...
qtquicktimeline/.git/hooks/commit-msg: Assembler messages:
qtquicktimeline/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtquicktimeline/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtquicktimeline/.git/hooks/commit-msg:29: Error: bad expression
qtquicktimeline/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtquicktimeline/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtquicktimeline/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtquicktimeline/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtquicktimeline/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtquicktimeline/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtquicktimeline/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtquicktimeline/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtquicktimeline/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtquicktimeline/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtquicktimeline/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtquicktimeline/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtquicktimeline/.git/hooks/commit-msg:47: Error: bad expression
qtquicktimeline/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtquicktimeline/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtquicktimeline/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtquicktimeline/.git/hooks/commit-msg:52: Error: bad expression
qtquicktimeline/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtquicktimeline/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtquicktimeline/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtquicktimeline/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtquicktimeline/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtquicktimeline/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtquicktimeline/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtquicktimeline/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtquicktimeline/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtquicktimeline/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtquicktimeline/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtquicktimeline/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtquicktimeline/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtquicktimeline/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtquicktimeline/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtquicktimeline/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtquicktimeline/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtquicktimeline/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtquicktimeline/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtquicktimeline/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtquicktimeline/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtquicktimeline/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtquicktimeline/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtquicktimeline/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtquicktimeline/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtquicktimeline/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtquicktimeline/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtquicktimeline/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtquicktimeline/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtquicktimeline/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtquicktimeline/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtquicktimeline/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtquicktimeline/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtquicktimeline/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtquicktimeline/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtquicktimeline/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtquicktimeline/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtquicktimeline/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtquicktimeline/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtquicktimeline/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtquicktimeline/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtquicktimeline/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtquicktimeline/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtquicktimeline/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtquicktimeline/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtquicktimeline/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtquicktimeline/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtquicktimeline/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtquicktimeline/.git/hooks/post-commit ...
qtquicktimeline/.git/hooks/post-commit: Assembler messages:
qtquicktimeline/.git/hooks/post-commit: Warning: end of file in comment
qtquicktimeline/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtquicktimeline/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtquicktimeline/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtremoteobjects/.git/hooks/commit-msg ...
qtremoteobjects/.git/hooks/commit-msg: Assembler messages:
qtremoteobjects/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtremoteobjects/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtremoteobjects/.git/hooks/commit-msg:29: Error: bad expression
qtremoteobjects/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtremoteobjects/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtremoteobjects/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtremoteobjects/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtremoteobjects/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtremoteobjects/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtremoteobjects/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtremoteobjects/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtremoteobjects/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtremoteobjects/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtremoteobjects/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtremoteobjects/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtremoteobjects/.git/hooks/commit-msg:47: Error: bad expression
qtremoteobjects/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtremoteobjects/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtremoteobjects/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtremoteobjects/.git/hooks/commit-msg:52: Error: bad expression
qtremoteobjects/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtremoteobjects/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtremoteobjects/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtremoteobjects/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtremoteobjects/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtremoteobjects/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtremoteobjects/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtremoteobjects/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtremoteobjects/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtremoteobjects/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtremoteobjects/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtremoteobjects/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtremoteobjects/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtremoteobjects/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtremoteobjects/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtremoteobjects/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtremoteobjects/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtremoteobjects/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtremoteobjects/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtremoteobjects/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtremoteobjects/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtremoteobjects/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtremoteobjects/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtremoteobjects/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtremoteobjects/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtremoteobjects/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtremoteobjects/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtremoteobjects/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtremoteobjects/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtremoteobjects/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtremoteobjects/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtremoteobjects/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtremoteobjects/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtremoteobjects/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtremoteobjects/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtremoteobjects/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtremoteobjects/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtremoteobjects/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtremoteobjects/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtremoteobjects/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtremoteobjects/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtremoteobjects/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtremoteobjects/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtremoteobjects/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtremoteobjects/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtremoteobjects/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtremoteobjects/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtremoteobjects/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtremoteobjects/.git/hooks/post-commit ...
qtremoteobjects/.git/hooks/post-commit: Assembler messages:
qtremoteobjects/.git/hooks/post-commit: Warning: end of file in comment
qtremoteobjects/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtremoteobjects/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtremoteobjects/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtrepotools/.git/hooks/commit-msg ...
qtrepotools/.git/hooks/commit-msg: Assembler messages:
qtrepotools/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtrepotools/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtrepotools/.git/hooks/commit-msg:29: Error: bad expression
qtrepotools/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtrepotools/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtrepotools/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtrepotools/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtrepotools/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtrepotools/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtrepotools/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtrepotools/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtrepotools/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtrepotools/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtrepotools/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtrepotools/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtrepotools/.git/hooks/commit-msg:47: Error: bad expression
qtrepotools/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtrepotools/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtrepotools/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtrepotools/.git/hooks/commit-msg:52: Error: bad expression
qtrepotools/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtrepotools/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtrepotools/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtrepotools/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtrepotools/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtrepotools/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtrepotools/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtrepotools/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtrepotools/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtrepotools/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtrepotools/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtrepotools/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtrepotools/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtrepotools/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtrepotools/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtrepotools/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtrepotools/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtrepotools/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtrepotools/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtrepotools/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtrepotools/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtrepotools/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtrepotools/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtrepotools/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtrepotools/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtrepotools/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtrepotools/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtrepotools/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtrepotools/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtrepotools/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtrepotools/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtrepotools/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtrepotools/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtrepotools/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtrepotools/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtrepotools/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtrepotools/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtrepotools/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtrepotools/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtrepotools/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtrepotools/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtrepotools/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtrepotools/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtrepotools/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtrepotools/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtrepotools/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtrepotools/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtrepotools/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtrepotools/.git/hooks/post-commit ...
qtrepotools/.git/hooks/post-commit: Assembler messages:
qtrepotools/.git/hooks/post-commit: Warning: end of file in comment
qtrepotools/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtrepotools/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtrepotools/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtscript/.git/hooks/commit-msg ...
qtscript/.git/hooks/commit-msg: Assembler messages:
qtscript/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtscript/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtscript/.git/hooks/commit-msg:29: Error: bad expression
qtscript/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtscript/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtscript/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtscript/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtscript/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtscript/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtscript/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtscript/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtscript/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtscript/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtscript/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtscript/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtscript/.git/hooks/commit-msg:47: Error: bad expression
qtscript/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtscript/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtscript/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtscript/.git/hooks/commit-msg:52: Error: bad expression
qtscript/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtscript/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtscript/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtscript/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtscript/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtscript/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtscript/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtscript/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtscript/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtscript/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtscript/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtscript/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtscript/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtscript/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtscript/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtscript/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtscript/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtscript/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtscript/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtscript/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtscript/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtscript/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtscript/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtscript/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtscript/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtscript/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtscript/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtscript/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtscript/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtscript/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtscript/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtscript/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtscript/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtscript/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtscript/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtscript/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtscript/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtscript/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtscript/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtscript/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtscript/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtscript/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtscript/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtscript/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtscript/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtscript/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtscript/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtscript/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtscript/.git/hooks/post-commit ...
qtscript/.git/hooks/post-commit: Assembler messages:
qtscript/.git/hooks/post-commit: Warning: end of file in comment
qtscript/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtscript/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtscript/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtscxml/.git/hooks/commit-msg ...
qtscxml/.git/hooks/commit-msg: Assembler messages:
qtscxml/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtscxml/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtscxml/.git/hooks/commit-msg:29: Error: bad expression
qtscxml/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtscxml/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtscxml/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtscxml/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtscxml/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtscxml/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtscxml/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtscxml/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtscxml/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtscxml/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtscxml/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtscxml/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtscxml/.git/hooks/commit-msg:47: Error: bad expression
qtscxml/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtscxml/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtscxml/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtscxml/.git/hooks/commit-msg:52: Error: bad expression
qtscxml/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtscxml/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtscxml/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtscxml/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtscxml/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtscxml/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtscxml/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtscxml/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtscxml/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtscxml/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtscxml/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtscxml/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtscxml/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtscxml/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtscxml/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtscxml/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtscxml/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtscxml/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtscxml/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtscxml/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtscxml/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtscxml/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtscxml/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtscxml/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtscxml/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtscxml/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtscxml/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtscxml/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtscxml/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtscxml/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtscxml/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtscxml/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtscxml/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtscxml/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtscxml/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtscxml/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtscxml/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtscxml/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtscxml/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtscxml/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtscxml/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtscxml/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtscxml/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtscxml/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtscxml/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtscxml/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtscxml/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtscxml/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtscxml/.git/hooks/post-commit ...
qtscxml/.git/hooks/post-commit: Assembler messages:
qtscxml/.git/hooks/post-commit: Warning: end of file in comment
qtscxml/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtscxml/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtscxml/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtsensors/.git/hooks/commit-msg ...
qtsensors/.git/hooks/commit-msg: Assembler messages:
qtsensors/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtsensors/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtsensors/.git/hooks/commit-msg:29: Error: bad expression
qtsensors/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtsensors/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtsensors/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtsensors/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtsensors/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtsensors/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtsensors/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtsensors/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtsensors/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtsensors/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtsensors/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtsensors/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtsensors/.git/hooks/commit-msg:47: Error: bad expression
qtsensors/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtsensors/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtsensors/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtsensors/.git/hooks/commit-msg:52: Error: bad expression
qtsensors/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtsensors/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtsensors/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtsensors/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtsensors/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtsensors/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtsensors/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtsensors/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtsensors/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtsensors/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtsensors/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtsensors/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtsensors/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtsensors/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtsensors/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtsensors/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtsensors/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtsensors/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtsensors/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtsensors/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtsensors/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtsensors/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtsensors/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtsensors/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtsensors/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtsensors/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtsensors/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtsensors/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtsensors/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtsensors/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtsensors/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtsensors/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtsensors/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtsensors/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtsensors/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtsensors/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtsensors/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtsensors/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtsensors/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtsensors/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtsensors/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtsensors/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtsensors/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtsensors/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtsensors/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtsensors/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtsensors/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtsensors/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtsensors/.git/hooks/post-commit ...
qtsensors/.git/hooks/post-commit: Assembler messages:
qtsensors/.git/hooks/post-commit: Warning: end of file in comment
qtsensors/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtsensors/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtsensors/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtserialbus/.git/hooks/commit-msg ...
qtserialbus/.git/hooks/commit-msg: Assembler messages:
qtserialbus/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtserialbus/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtserialbus/.git/hooks/commit-msg:29: Error: bad expression
qtserialbus/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtserialbus/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtserialbus/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtserialbus/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtserialbus/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtserialbus/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtserialbus/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtserialbus/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtserialbus/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtserialbus/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtserialbus/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtserialbus/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtserialbus/.git/hooks/commit-msg:47: Error: bad expression
qtserialbus/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtserialbus/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtserialbus/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtserialbus/.git/hooks/commit-msg:52: Error: bad expression
qtserialbus/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtserialbus/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtserialbus/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtserialbus/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtserialbus/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtserialbus/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtserialbus/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtserialbus/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtserialbus/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtserialbus/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtserialbus/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtserialbus/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtserialbus/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtserialbus/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtserialbus/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtserialbus/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtserialbus/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtserialbus/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtserialbus/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtserialbus/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtserialbus/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtserialbus/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtserialbus/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtserialbus/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtserialbus/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtserialbus/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtserialbus/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtserialbus/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtserialbus/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtserialbus/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtserialbus/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtserialbus/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtserialbus/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtserialbus/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtserialbus/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtserialbus/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtserialbus/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtserialbus/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtserialbus/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtserialbus/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtserialbus/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtserialbus/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtserialbus/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtserialbus/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtserialbus/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtserialbus/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtserialbus/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtserialbus/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtserialbus/.git/hooks/post-commit ...
qtserialbus/.git/hooks/post-commit: Assembler messages:
qtserialbus/.git/hooks/post-commit: Warning: end of file in comment
qtserialbus/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtserialbus/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtserialbus/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtserialport/.git/hooks/commit-msg ...
qtserialport/.git/hooks/commit-msg: Assembler messages:
qtserialport/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtserialport/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtserialport/.git/hooks/commit-msg:29: Error: bad expression
qtserialport/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtserialport/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtserialport/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtserialport/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtserialport/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtserialport/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtserialport/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtserialport/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtserialport/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtserialport/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtserialport/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtserialport/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtserialport/.git/hooks/commit-msg:47: Error: bad expression
qtserialport/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtserialport/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtserialport/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtserialport/.git/hooks/commit-msg:52: Error: bad expression
qtserialport/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtserialport/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtserialport/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtserialport/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtserialport/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtserialport/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtserialport/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtserialport/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtserialport/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtserialport/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtserialport/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtserialport/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtserialport/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtserialport/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtserialport/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtserialport/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtserialport/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtserialport/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtserialport/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtserialport/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtserialport/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtserialport/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtserialport/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtserialport/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtserialport/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtserialport/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtserialport/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtserialport/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtserialport/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtserialport/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtserialport/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtserialport/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtserialport/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtserialport/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtserialport/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtserialport/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtserialport/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtserialport/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtserialport/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtserialport/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtserialport/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtserialport/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtserialport/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtserialport/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtserialport/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtserialport/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtserialport/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtserialport/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtserialport/.git/hooks/post-commit ...
qtserialport/.git/hooks/post-commit: Assembler messages:
qtserialport/.git/hooks/post-commit: Warning: end of file in comment
qtserialport/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtserialport/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtserialport/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtspeech/.git/hooks/commit-msg ...
qtspeech/.git/hooks/commit-msg: Assembler messages:
qtspeech/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtspeech/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtspeech/.git/hooks/commit-msg:29: Error: bad expression
qtspeech/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtspeech/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtspeech/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtspeech/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtspeech/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtspeech/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtspeech/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtspeech/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtspeech/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtspeech/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtspeech/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtspeech/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtspeech/.git/hooks/commit-msg:47: Error: bad expression
qtspeech/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtspeech/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtspeech/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtspeech/.git/hooks/commit-msg:52: Error: bad expression
qtspeech/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtspeech/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtspeech/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtspeech/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtspeech/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtspeech/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtspeech/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtspeech/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtspeech/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtspeech/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtspeech/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtspeech/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtspeech/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtspeech/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtspeech/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtspeech/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtspeech/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtspeech/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtspeech/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtspeech/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtspeech/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtspeech/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtspeech/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtspeech/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtspeech/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtspeech/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtspeech/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtspeech/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtspeech/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtspeech/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtspeech/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtspeech/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtspeech/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtspeech/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtspeech/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtspeech/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtspeech/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtspeech/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtspeech/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtspeech/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtspeech/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtspeech/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtspeech/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtspeech/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtspeech/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtspeech/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtspeech/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtspeech/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtspeech/.git/hooks/post-commit ...
qtspeech/.git/hooks/post-commit: Assembler messages:
qtspeech/.git/hooks/post-commit: Warning: end of file in comment
qtspeech/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtspeech/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtspeech/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtsvg/.git/hooks/commit-msg ...
qtsvg/.git/hooks/commit-msg: Assembler messages:
qtsvg/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtsvg/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtsvg/.git/hooks/commit-msg:29: Error: bad expression
qtsvg/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtsvg/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtsvg/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtsvg/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtsvg/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtsvg/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtsvg/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtsvg/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtsvg/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtsvg/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtsvg/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtsvg/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtsvg/.git/hooks/commit-msg:47: Error: bad expression
qtsvg/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtsvg/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtsvg/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtsvg/.git/hooks/commit-msg:52: Error: bad expression
qtsvg/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtsvg/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtsvg/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtsvg/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtsvg/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtsvg/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtsvg/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtsvg/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtsvg/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtsvg/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtsvg/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtsvg/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtsvg/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtsvg/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtsvg/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtsvg/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtsvg/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtsvg/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtsvg/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtsvg/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtsvg/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtsvg/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtsvg/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtsvg/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtsvg/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtsvg/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtsvg/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtsvg/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtsvg/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtsvg/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtsvg/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtsvg/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtsvg/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtsvg/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtsvg/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtsvg/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtsvg/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtsvg/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtsvg/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtsvg/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtsvg/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtsvg/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtsvg/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtsvg/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtsvg/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtsvg/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtsvg/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtsvg/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtsvg/.git/hooks/post-commit ...
qtsvg/.git/hooks/post-commit: Assembler messages:
qtsvg/.git/hooks/post-commit: Warning: end of file in comment
qtsvg/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtsvg/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtsvg/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qttools/.git/hooks/commit-msg ...
qttools/.git/hooks/commit-msg: Assembler messages:
qttools/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qttools/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qttools/.git/hooks/commit-msg:29: Error: bad expression
qttools/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qttools/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qttools/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qttools/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qttools/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qttools/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qttools/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qttools/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qttools/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qttools/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qttools/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qttools/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qttools/.git/hooks/commit-msg:47: Error: bad expression
qttools/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qttools/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qttools/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qttools/.git/hooks/commit-msg:52: Error: bad expression
qttools/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qttools/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qttools/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qttools/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qttools/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qttools/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qttools/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qttools/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qttools/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qttools/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qttools/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qttools/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qttools/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qttools/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qttools/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qttools/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qttools/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qttools/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qttools/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qttools/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qttools/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qttools/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qttools/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qttools/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qttools/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qttools/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qttools/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qttools/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qttools/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qttools/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qttools/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qttools/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qttools/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qttools/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qttools/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qttools/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qttools/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qttools/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qttools/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qttools/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qttools/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qttools/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qttools/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qttools/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qttools/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qttools/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qttools/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qttools/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qttools/.git/hooks/post-commit ...
qttools/.git/hooks/post-commit: Assembler messages:
qttools/.git/hooks/post-commit: Warning: end of file in comment
qttools/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qttools/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qttools/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qttranslations/.git/hooks/commit-msg ...
qttranslations/.git/hooks/commit-msg: Assembler messages:
qttranslations/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qttranslations/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qttranslations/.git/hooks/commit-msg:29: Error: bad expression
qttranslations/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qttranslations/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qttranslations/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qttranslations/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qttranslations/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qttranslations/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qttranslations/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qttranslations/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qttranslations/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qttranslations/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qttranslations/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qttranslations/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qttranslations/.git/hooks/commit-msg:47: Error: bad expression
qttranslations/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qttranslations/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qttranslations/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qttranslations/.git/hooks/commit-msg:52: Error: bad expression
qttranslations/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qttranslations/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qttranslations/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qttranslations/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qttranslations/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qttranslations/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qttranslations/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qttranslations/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qttranslations/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qttranslations/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qttranslations/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qttranslations/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qttranslations/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qttranslations/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qttranslations/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qttranslations/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qttranslations/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qttranslations/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qttranslations/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qttranslations/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qttranslations/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qttranslations/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qttranslations/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qttranslations/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qttranslations/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qttranslations/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qttranslations/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qttranslations/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qttranslations/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qttranslations/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qttranslations/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qttranslations/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qttranslations/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qttranslations/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qttranslations/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qttranslations/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qttranslations/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qttranslations/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qttranslations/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qttranslations/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qttranslations/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qttranslations/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qttranslations/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qttranslations/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qttranslations/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qttranslations/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qttranslations/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qttranslations/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qttranslations/.git/hooks/post-commit ...
qttranslations/.git/hooks/post-commit: Assembler messages:
qttranslations/.git/hooks/post-commit: Warning: end of file in comment
qttranslations/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qttranslations/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qttranslations/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtvirtualkeyboard/.git/hooks/commit-msg ...
qtvirtualkeyboard/.git/hooks/commit-msg: Assembler messages:
qtvirtualkeyboard/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtvirtualkeyboard/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtvirtualkeyboard/.git/hooks/commit-msg:29: Error: bad expression
qtvirtualkeyboard/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtvirtualkeyboard/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtvirtualkeyboard/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtvirtualkeyboard/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtvirtualkeyboard/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtvirtualkeyboard/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtvirtualkeyboard/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtvirtualkeyboard/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtvirtualkeyboard/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtvirtualkeyboard/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtvirtualkeyboard/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtvirtualkeyboard/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtvirtualkeyboard/.git/hooks/commit-msg:47: Error: bad expression
qtvirtualkeyboard/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtvirtualkeyboard/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtvirtualkeyboard/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtvirtualkeyboard/.git/hooks/commit-msg:52: Error: bad expression
qtvirtualkeyboard/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtvirtualkeyboard/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtvirtualkeyboard/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtvirtualkeyboard/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtvirtualkeyboard/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtvirtualkeyboard/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtvirtualkeyboard/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtvirtualkeyboard/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtvirtualkeyboard/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtvirtualkeyboard/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtvirtualkeyboard/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtvirtualkeyboard/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtvirtualkeyboard/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtvirtualkeyboard/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtvirtualkeyboard/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtvirtualkeyboard/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtvirtualkeyboard/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtvirtualkeyboard/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtvirtualkeyboard/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtvirtualkeyboard/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtvirtualkeyboard/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtvirtualkeyboard/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtvirtualkeyboard/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtvirtualkeyboard/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtvirtualkeyboard/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtvirtualkeyboard/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtvirtualkeyboard/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtvirtualkeyboard/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtvirtualkeyboard/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtvirtualkeyboard/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtvirtualkeyboard/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtvirtualkeyboard/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtvirtualkeyboard/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtvirtualkeyboard/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtvirtualkeyboard/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtvirtualkeyboard/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtvirtualkeyboard/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtvirtualkeyboard/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtvirtualkeyboard/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtvirtualkeyboard/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtvirtualkeyboard/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtvirtualkeyboard/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtvirtualkeyboard/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtvirtualkeyboard/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtvirtualkeyboard/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtvirtualkeyboard/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtvirtualkeyboard/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtvirtualkeyboard/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtvirtualkeyboard/.git/hooks/post-commit ...
qtvirtualkeyboard/.git/hooks/post-commit: Assembler messages:
qtvirtualkeyboard/.git/hooks/post-commit: Warning: end of file in comment
qtvirtualkeyboard/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtvirtualkeyboard/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtvirtualkeyboard/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwayland/.git/hooks/commit-msg ...
qtwayland/.git/hooks/commit-msg: Assembler messages:
qtwayland/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtwayland/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtwayland/.git/hooks/commit-msg:29: Error: bad expression
qtwayland/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtwayland/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtwayland/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtwayland/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtwayland/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtwayland/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtwayland/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtwayland/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtwayland/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtwayland/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtwayland/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtwayland/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtwayland/.git/hooks/commit-msg:47: Error: bad expression
qtwayland/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtwayland/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtwayland/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtwayland/.git/hooks/commit-msg:52: Error: bad expression
qtwayland/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtwayland/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtwayland/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtwayland/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtwayland/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtwayland/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtwayland/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtwayland/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtwayland/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtwayland/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtwayland/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtwayland/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtwayland/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtwayland/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtwayland/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtwayland/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtwayland/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtwayland/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtwayland/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtwayland/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtwayland/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtwayland/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtwayland/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtwayland/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtwayland/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtwayland/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtwayland/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtwayland/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtwayland/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwayland/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtwayland/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtwayland/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwayland/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtwayland/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtwayland/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtwayland/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtwayland/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtwayland/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtwayland/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtwayland/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtwayland/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtwayland/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtwayland/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtwayland/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtwayland/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtwayland/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtwayland/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtwayland/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwayland/.git/hooks/post-commit ...
qtwayland/.git/hooks/post-commit: Assembler messages:
qtwayland/.git/hooks/post-commit: Warning: end of file in comment
qtwayland/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtwayland/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtwayland/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwebchannel/.git/hooks/commit-msg ...
qtwebchannel/.git/hooks/commit-msg: Assembler messages:
qtwebchannel/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtwebchannel/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtwebchannel/.git/hooks/commit-msg:29: Error: bad expression
qtwebchannel/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtwebchannel/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtwebchannel/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtwebchannel/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtwebchannel/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtwebchannel/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtwebchannel/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtwebchannel/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtwebchannel/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtwebchannel/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtwebchannel/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtwebchannel/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtwebchannel/.git/hooks/commit-msg:47: Error: bad expression
qtwebchannel/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtwebchannel/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtwebchannel/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtwebchannel/.git/hooks/commit-msg:52: Error: bad expression
qtwebchannel/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtwebchannel/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtwebchannel/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtwebchannel/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtwebchannel/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtwebchannel/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtwebchannel/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtwebchannel/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtwebchannel/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtwebchannel/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtwebchannel/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtwebchannel/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtwebchannel/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtwebchannel/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtwebchannel/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtwebchannel/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtwebchannel/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtwebchannel/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtwebchannel/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtwebchannel/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtwebchannel/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtwebchannel/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtwebchannel/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtwebchannel/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtwebchannel/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtwebchannel/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtwebchannel/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtwebchannel/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtwebchannel/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwebchannel/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtwebchannel/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtwebchannel/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwebchannel/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtwebchannel/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtwebchannel/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtwebchannel/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtwebchannel/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtwebchannel/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtwebchannel/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtwebchannel/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtwebchannel/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtwebchannel/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtwebchannel/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtwebchannel/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtwebchannel/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtwebchannel/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtwebchannel/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtwebchannel/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwebchannel/.git/hooks/post-commit ...
qtwebchannel/.git/hooks/post-commit: Assembler messages:
qtwebchannel/.git/hooks/post-commit: Warning: end of file in comment
qtwebchannel/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtwebchannel/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtwebchannel/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwebengine/.git/hooks/commit-msg ...
qtwebengine/.git/hooks/commit-msg: Assembler messages:
qtwebengine/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtwebengine/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtwebengine/.git/hooks/commit-msg:29: Error: bad expression
qtwebengine/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtwebengine/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtwebengine/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtwebengine/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtwebengine/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtwebengine/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtwebengine/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtwebengine/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtwebengine/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtwebengine/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtwebengine/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtwebengine/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtwebengine/.git/hooks/commit-msg:47: Error: bad expression
qtwebengine/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtwebengine/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtwebengine/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtwebengine/.git/hooks/commit-msg:52: Error: bad expression
qtwebengine/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtwebengine/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtwebengine/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtwebengine/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtwebengine/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtwebengine/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtwebengine/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtwebengine/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtwebengine/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtwebengine/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtwebengine/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtwebengine/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtwebengine/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtwebengine/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtwebengine/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtwebengine/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtwebengine/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtwebengine/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtwebengine/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtwebengine/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtwebengine/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtwebengine/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtwebengine/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtwebengine/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtwebengine/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtwebengine/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtwebengine/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtwebengine/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtwebengine/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwebengine/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtwebengine/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtwebengine/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwebengine/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtwebengine/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtwebengine/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtwebengine/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtwebengine/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtwebengine/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtwebengine/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtwebengine/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtwebengine/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtwebengine/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtwebengine/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtwebengine/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtwebengine/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtwebengine/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtwebengine/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtwebengine/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwebengine/.git/hooks/post-commit ...
qtwebengine/.git/hooks/post-commit: Assembler messages:
qtwebengine/.git/hooks/post-commit: Warning: end of file in comment
qtwebengine/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtwebengine/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtwebengine/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwebglplugin/.git/hooks/commit-msg ...
qtwebglplugin/.git/hooks/commit-msg: Assembler messages:
qtwebglplugin/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtwebglplugin/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtwebglplugin/.git/hooks/commit-msg:29: Error: bad expression
qtwebglplugin/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtwebglplugin/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtwebglplugin/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtwebglplugin/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtwebglplugin/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtwebglplugin/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtwebglplugin/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtwebglplugin/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtwebglplugin/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtwebglplugin/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtwebglplugin/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtwebglplugin/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtwebglplugin/.git/hooks/commit-msg:47: Error: bad expression
qtwebglplugin/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtwebglplugin/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtwebglplugin/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtwebglplugin/.git/hooks/commit-msg:52: Error: bad expression
qtwebglplugin/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtwebglplugin/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtwebglplugin/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtwebglplugin/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtwebglplugin/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtwebglplugin/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtwebglplugin/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtwebglplugin/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtwebglplugin/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtwebglplugin/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtwebglplugin/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtwebglplugin/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtwebglplugin/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtwebglplugin/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtwebglplugin/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtwebglplugin/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtwebglplugin/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtwebglplugin/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtwebglplugin/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtwebglplugin/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtwebglplugin/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtwebglplugin/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtwebglplugin/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtwebglplugin/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtwebglplugin/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtwebglplugin/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtwebglplugin/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtwebglplugin/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtwebglplugin/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwebglplugin/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtwebglplugin/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtwebglplugin/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwebglplugin/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtwebglplugin/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtwebglplugin/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtwebglplugin/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtwebglplugin/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtwebglplugin/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtwebglplugin/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtwebglplugin/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtwebglplugin/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtwebglplugin/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtwebglplugin/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtwebglplugin/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtwebglplugin/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtwebglplugin/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtwebglplugin/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtwebglplugin/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwebglplugin/.git/hooks/post-commit ...
qtwebglplugin/.git/hooks/post-commit: Assembler messages:
qtwebglplugin/.git/hooks/post-commit: Warning: end of file in comment
qtwebglplugin/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtwebglplugin/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtwebglplugin/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwebsockets/.git/hooks/commit-msg ...
qtwebsockets/.git/hooks/commit-msg: Assembler messages:
qtwebsockets/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtwebsockets/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtwebsockets/.git/hooks/commit-msg:29: Error: bad expression
qtwebsockets/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtwebsockets/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtwebsockets/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtwebsockets/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtwebsockets/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtwebsockets/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtwebsockets/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtwebsockets/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtwebsockets/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtwebsockets/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtwebsockets/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtwebsockets/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtwebsockets/.git/hooks/commit-msg:47: Error: bad expression
qtwebsockets/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtwebsockets/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtwebsockets/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtwebsockets/.git/hooks/commit-msg:52: Error: bad expression
qtwebsockets/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtwebsockets/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtwebsockets/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtwebsockets/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtwebsockets/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtwebsockets/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtwebsockets/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtwebsockets/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtwebsockets/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtwebsockets/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtwebsockets/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtwebsockets/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtwebsockets/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtwebsockets/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtwebsockets/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtwebsockets/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtwebsockets/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtwebsockets/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtwebsockets/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtwebsockets/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtwebsockets/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtwebsockets/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtwebsockets/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtwebsockets/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtwebsockets/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtwebsockets/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtwebsockets/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtwebsockets/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtwebsockets/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwebsockets/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtwebsockets/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtwebsockets/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwebsockets/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtwebsockets/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtwebsockets/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtwebsockets/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtwebsockets/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtwebsockets/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtwebsockets/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtwebsockets/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtwebsockets/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtwebsockets/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtwebsockets/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtwebsockets/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtwebsockets/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtwebsockets/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtwebsockets/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtwebsockets/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwebsockets/.git/hooks/post-commit ...
qtwebsockets/.git/hooks/post-commit: Assembler messages:
qtwebsockets/.git/hooks/post-commit: Warning: end of file in comment
qtwebsockets/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtwebsockets/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtwebsockets/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwebview/.git/hooks/commit-msg ...
qtwebview/.git/hooks/commit-msg: Assembler messages:
qtwebview/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtwebview/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtwebview/.git/hooks/commit-msg:29: Error: bad expression
qtwebview/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtwebview/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtwebview/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtwebview/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtwebview/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtwebview/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtwebview/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtwebview/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtwebview/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtwebview/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtwebview/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtwebview/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtwebview/.git/hooks/commit-msg:47: Error: bad expression
qtwebview/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtwebview/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtwebview/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtwebview/.git/hooks/commit-msg:52: Error: bad expression
qtwebview/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtwebview/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtwebview/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtwebview/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtwebview/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtwebview/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtwebview/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtwebview/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtwebview/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtwebview/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtwebview/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtwebview/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtwebview/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtwebview/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtwebview/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtwebview/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtwebview/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtwebview/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtwebview/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtwebview/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtwebview/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtwebview/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtwebview/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtwebview/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtwebview/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtwebview/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtwebview/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtwebview/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtwebview/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwebview/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtwebview/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtwebview/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwebview/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtwebview/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtwebview/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtwebview/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtwebview/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtwebview/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtwebview/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtwebview/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtwebview/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtwebview/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtwebview/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtwebview/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtwebview/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtwebview/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtwebview/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtwebview/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwebview/.git/hooks/post-commit ...
qtwebview/.git/hooks/post-commit: Assembler messages:
qtwebview/.git/hooks/post-commit: Warning: end of file in comment
qtwebview/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtwebview/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtwebview/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwinextras/.git/hooks/commit-msg ...
qtwinextras/.git/hooks/commit-msg: Assembler messages:
qtwinextras/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtwinextras/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtwinextras/.git/hooks/commit-msg:29: Error: bad expression
qtwinextras/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtwinextras/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtwinextras/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtwinextras/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtwinextras/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtwinextras/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtwinextras/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtwinextras/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtwinextras/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtwinextras/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtwinextras/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtwinextras/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtwinextras/.git/hooks/commit-msg:47: Error: bad expression
qtwinextras/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtwinextras/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtwinextras/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtwinextras/.git/hooks/commit-msg:52: Error: bad expression
qtwinextras/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtwinextras/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtwinextras/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtwinextras/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtwinextras/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtwinextras/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtwinextras/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtwinextras/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtwinextras/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtwinextras/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtwinextras/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtwinextras/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtwinextras/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtwinextras/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtwinextras/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtwinextras/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtwinextras/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtwinextras/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtwinextras/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtwinextras/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtwinextras/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtwinextras/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtwinextras/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtwinextras/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtwinextras/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtwinextras/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtwinextras/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtwinextras/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtwinextras/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwinextras/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtwinextras/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtwinextras/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtwinextras/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtwinextras/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtwinextras/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtwinextras/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtwinextras/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtwinextras/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtwinextras/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtwinextras/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtwinextras/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtwinextras/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtwinextras/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtwinextras/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtwinextras/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtwinextras/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtwinextras/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtwinextras/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtwinextras/.git/hooks/post-commit ...
qtwinextras/.git/hooks/post-commit: Assembler messages:
qtwinextras/.git/hooks/post-commit: Warning: end of file in comment
qtwinextras/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtwinextras/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtwinextras/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtx11extras/.git/hooks/commit-msg ...
qtx11extras/.git/hooks/commit-msg: Assembler messages:
qtx11extras/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtx11extras/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtx11extras/.git/hooks/commit-msg:29: Error: bad expression
qtx11extras/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtx11extras/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtx11extras/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtx11extras/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtx11extras/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtx11extras/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtx11extras/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtx11extras/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtx11extras/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtx11extras/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtx11extras/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtx11extras/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtx11extras/.git/hooks/commit-msg:47: Error: bad expression
qtx11extras/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtx11extras/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtx11extras/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtx11extras/.git/hooks/commit-msg:52: Error: bad expression
qtx11extras/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtx11extras/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtx11extras/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtx11extras/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtx11extras/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtx11extras/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtx11extras/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtx11extras/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtx11extras/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtx11extras/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtx11extras/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtx11extras/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtx11extras/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtx11extras/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtx11extras/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtx11extras/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtx11extras/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtx11extras/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtx11extras/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtx11extras/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtx11extras/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtx11extras/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtx11extras/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtx11extras/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtx11extras/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtx11extras/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtx11extras/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtx11extras/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtx11extras/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtx11extras/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtx11extras/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtx11extras/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtx11extras/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtx11extras/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtx11extras/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtx11extras/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtx11extras/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtx11extras/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtx11extras/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtx11extras/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtx11extras/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtx11extras/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtx11extras/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtx11extras/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtx11extras/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtx11extras/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtx11extras/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtx11extras/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtx11extras/.git/hooks/post-commit ...
qtx11extras/.git/hooks/post-commit: Assembler messages:
qtx11extras/.git/hooks/post-commit: Warning: end of file in comment
qtx11extras/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtx11extras/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtx11extras/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/gerrit_commit_msg_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtxmlpatterns/.git/hooks/commit-msg ...
qtxmlpatterns/.git/hooks/commit-msg: Assembler messages:
qtxmlpatterns/.git/hooks/commit-msg:21: Error: no such instruction: `unset GREP_OPTIONS'
qtxmlpatterns/.git/hooks/commit-msg:28: Error: invalid character '(' in mnemonic
qtxmlpatterns/.git/hooks/commit-msg:29: Error: bad expression
qtxmlpatterns/.git/hooks/commit-msg:29: Error: junk at end of line, first unrecognized character is `s'
qtxmlpatterns/.git/hooks/commit-msg:30: Error: no such instruction: `s///'
qtxmlpatterns/.git/hooks/commit-msg:31: Error: no such instruction: `q'
qtxmlpatterns/.git/hooks/commit-msg:32: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:35: Error: junk at end of line, first unrecognized character is `3'
qtxmlpatterns/.git/hooks/commit-msg:36: Error: no such instruction: `if test -z "$clean_message"'
qtxmlpatterns/.git/hooks/commit-msg:37: Error: no such instruction: `then'
qtxmlpatterns/.git/hooks/commit-msg:38: Error: no such instruction: `return'
qtxmlpatterns/.git/hooks/commit-msg:39: Error: no such instruction: `fi'
qtxmlpatterns/.git/hooks/commit-msg:42: Error: no such instruction: `if grep -i 94Change-Id:32"$MSG">/dev/null'
qtxmlpatterns/.git/hooks/commit-msg:43: Error: no such instruction: `then'
qtxmlpatterns/.git/hooks/commit-msg:44: Error: no such instruction: `return'
qtxmlpatterns/.git/hooks/commit-msg:45: Error: no such instruction: `fi'
qtxmlpatterns/.git/hooks/commit-msg:47: Error: bad expression
qtxmlpatterns/.git/hooks/commit-msg:47: Error: junk at end of line, first unrecognized character is `_'
qtxmlpatterns/.git/hooks/commit-msg:50: Error: no such instruction: `if [ -x/usr/xpg4/bin/awk]'
qtxmlpatterns/.git/hooks/commit-msg:50: Error: no such instruction: `then'
qtxmlpatterns/.git/hooks/commit-msg:52: Error: bad expression
qtxmlpatterns/.git/hooks/commit-msg:52: Error: junk at end of line, first unrecognized character is `u'
qtxmlpatterns/.git/hooks/commit-msg:53: Error: no such instruction: `fi'
qtxmlpatterns/.git/hooks/commit-msg:64: Error: invalid character '$' in mnemonic
qtxmlpatterns/.git/hooks/commit-msg:70: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:80: Error: no such instruction: `while (getline){ }'
qtxmlpatterns/.git/hooks/commit-msg:81: Error: no such instruction: `next'
qtxmlpatterns/.git/hooks/commit-msg:82: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:86: Error: invalid character '+' in mnemonic
qtxmlpatterns/.git/hooks/commit-msg:87: Error: no such instruction: `next'
qtxmlpatterns/.git/hooks/commit-msg:88: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:93: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:97: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:100: Error: junk at end of line, first unrecognized character is `('
qtxmlpatterns/.git/hooks/commit-msg:101: Error: no such instruction: `print lines'
qtxmlpatterns/.git/hooks/commit-msg:102: Error: no such instruction: `for (i=0'
qtxmlpatterns/.git/hooks/commit-msg:102: Error: no such instruction: `i <blankLines'
qtxmlpatterns/.git/hooks/commit-msg:102: Error: invalid character '+' in mnemonic
qtxmlpatterns/.git/hooks/commit-msg:103: Error: no such instruction: `print ""'
qtxmlpatterns/.git/hooks/commit-msg:104: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:110: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:113: Error: junk at end of line, first unrecognized character is `('
qtxmlpatterns/.git/hooks/commit-msg:115: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:117: Error: no such instruction: `{'
qtxmlpatterns/.git/hooks/commit-msg:119: Error: no such instruction: `if (footerComment==2){'
qtxmlpatterns/.git/hooks/commit-msg:121: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:122: Error: no such instruction: `if (lines!=""){'
qtxmlpatterns/.git/hooks/commit-msg:123: Error: junk at end of line, first unrecognized character is `"'
qtxmlpatterns/.git/hooks/commit-msg:124: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:125: Error: junk at end of line, first unrecognized character is `$'
qtxmlpatterns/.git/hooks/commit-msg:126: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:137: Error: no such instruction: `end {'
qtxmlpatterns/.git/hooks/commit-msg:139: Error: no such instruction: `if (isFooter==0){'
qtxmlpatterns/.git/hooks/commit-msg:140: Error: no such instruction: `print lines "\n"'
qtxmlpatterns/.git/hooks/commit-msg:142: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:143: Error: junk at end of line, first unrecognized character is `t'
qtxmlpatterns/.git/hooks/commit-msg:144: Error: junk at end of line, first unrecognized character is `('
qtxmlpatterns/.git/hooks/commit-msg:145: Error: no such instruction: `for (line=1'
qtxmlpatterns/.git/hooks/commit-msg:145: Error: no such instruction: `line <=numlines'
qtxmlpatterns/.git/hooks/commit-msg:145: Error: invalid character '+' in mnemonic
qtxmlpatterns/.git/hooks/commit-msg:146: Error: no such instruction: `if (unprinted&&match(tolower(footer[line]),changeIdAfter)!=1){'
qtxmlpatterns/.git/hooks/commit-msg:148: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtxmlpatterns/.git/hooks/commit-msg:149: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:150: Error: no such instruction: `print footer[line]'
qtxmlpatterns/.git/hooks/commit-msg:151: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:152: Error: no such instruction: `if (unprinted){'
qtxmlpatterns/.git/hooks/commit-msg:153: Error: no such instruction: `print "Change-Id: I'"$id"'"'
qtxmlpatterns/.git/hooks/commit-msg:154: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:155: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:156: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:157: Error: invalid character '(' in mnemonic
qtxmlpatterns/.git/hooks/commit-msg:158: Error: no such instruction: `echo "tree `git write-tree`"'
qtxmlpatterns/.git/hooks/commit-msg:159: Error: no such instruction: `if parent=`git rev-parse "HEAD^0"2>/dev/null`'
qtxmlpatterns/.git/hooks/commit-msg:160: Error: no such instruction: `then'
qtxmlpatterns/.git/hooks/commit-msg:161: Error: no such instruction: `echo "parent $parent"'
qtxmlpatterns/.git/hooks/commit-msg:162: Error: no such instruction: `fi'
qtxmlpatterns/.git/hooks/commit-msg:163: Error: no such instruction: `echo "author `git var GIT_AUTHOR_IDENT`"'
qtxmlpatterns/.git/hooks/commit-msg:164: Error: no such instruction: `echo "committer `git var GIT_COMMITTER_IDENT`"'
qtxmlpatterns/.git/hooks/commit-msg:165: Error: no such instruction: `echo'
qtxmlpatterns/.git/hooks/commit-msg:166: Error: no such instruction: `printf 37s32"$clean_message"'
qtxmlpatterns/.git/hooks/commit-msg:167: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:168: Error: invalid character '(' in mnemonic
qtxmlpatterns/.git/hooks/commit-msg:169: Error: no such instruction: `_gen_changeidinput |'
qtxmlpatterns/.git/hooks/commit-msg:170: Error: no such instruction: `git hash-object -t commit --stdin'
qtxmlpatterns/.git/hooks/commit-msg:171: Error: junk at end of line, first unrecognized character is `}'
qtxmlpatterns/.git/hooks/commit-msg:174: Error: no such instruction: `add_changeid'
qtxmlpatterns/.git/hooks/commit-msg: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ Aliasing /home/aiegoo/repos/projects/qt5/qtrepotools/git-hooks/git_post_commit_hook
Aliasing: 명령을 찾을 수 없습니다
aiegoo@tonylee:~/repos/projects/qt5$       as qtxmlpatterns/.git/hooks/post-commit ...
qtxmlpatterns/.git/hooks/post-commit: Assembler messages:
qtxmlpatterns/.git/hooks/post-commit: Warning: end of file in comment
qtxmlpatterns/.git/hooks/post-commit:14: Error: invalid character '(' in mnemonic
qtxmlpatterns/.git/hooks/post-commit:15: Error: no such instruction: `case $1 in'
qtxmlpatterns/.git/hooks/post-commit: Error: can't open ... for reading: 그런 파일이나 디렉터리가 없습니다
aiegoo@tonylee:~/repos/projects/qt5$ 
