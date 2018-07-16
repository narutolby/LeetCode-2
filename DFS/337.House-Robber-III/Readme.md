### 337.House-Robber-III

此题和其他House Robber系列不同,Ｈｏｕｓｅ的排列不是序列的数组，并不适合ＤＰ算法．这是因为ｌｅｆｔ的最佳策略，不仅取决于它的上级ｐａｒｅｎｔ的策略，而且还要取决于ｒｉｇｈｔ的策略．动态转移方程很难确定．

如果用常规的ＤＦＳ就很简单明了．每一个ｎｏｄｅ的策略（ｒｏｂ or not)都尝试一遍并向下延伸，最终取两者之间的最优．

注意的是，肯定会有很多重复搜索的情况．比如说节点Ａ取rob并向下ＤＦＳ的过程中，后续的节点Ｂ需要考察ｒｏｂ的决策；而Ａ取not rob并向下ＤＦＳ的过程中，后续的Ｂ可能也需要考察ｒｏｂ的决策．所以需要记忆化，将每个节点的决策及其价值都记录下来．