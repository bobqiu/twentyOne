# 生化21点游戏文档

## 概述
参考生化危机7 DLC 21点游戏写的一个游戏（规则有自己定义）

## 技术选型
* resteasy 2.2.1.GA
* mongoDB 3.4.2
* socketIO
* tomcat 8.x

## 游戏简述

* 标签：牌类，21点，回合制
* 卡牌类型：
    - 数字牌：代表1-11数字的卡牌各一张，共11张
    - 王牌：分n种类型
        + 抽牌类：抽卡阶段必抽到对应数字牌，如果牌堆里没有对应数字牌则什么都不会发生。对应数字为1-10各一张，共10张。
        + 抽牌类+：选择一个数字牌，抽卡阶段必抽到选择的数字牌，如果牌堆里没有选择的数字牌则什么都不会发生。共1张。
        + 攻击类：此卡在场上，拼点胜出时给对手增加伤害。增加1、2点伤害各两张，共4张。
        + 防御类：此卡在场上，拼点失败时自己遭受的伤害减1。共4张。
        + 