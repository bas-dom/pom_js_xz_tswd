#  部分冷却塔运行在50Hz，部分运行在30Hz #
## 提出 ##
  2017-06-29
  业主提出
  记录：golding

## 原因分析 ##
  经过实际验证，发现50Hz的那些点位设置不进DDC，比如 CTFanVSDFreqSetting16 设置为50Hz时，并不能成功。

  判断为 DDC点位被Ovverride

## 解决 ##
  远程登录到JCI Metasys系统，将这些被Override的点位Release（右键-Release Override）