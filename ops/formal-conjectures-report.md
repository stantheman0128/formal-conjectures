# formal-conjectures 貢獻報告（2026-09-13）

## STOP（2026-09-13）

**已停止對 google-deepmind/formal-conjectures 再開 Erdős statement PR。**

原因：maintainer 指出大量 statement-only 自動形式化目前不值得——審查成本太高。這已在 [google-deepmind/formal-conjectures#3422](https://github.com/google-deepmind/formal-conjectures/issues/3422) 與 Zulip 討論過（批次 AI 形式化會淹沒 review）。

本 session **不再** `gh pr create`、**不再** spawn Lean statement subagent。已開的 PR 維持現狀，等 operator。

Fork: https://github.com/stantheman0128/formal-conjectures
帳號: stantheman0128（Po-Han Shih）
目標 repo: google-deepmind/formal-conjectures
已開 PR：最後一波止於 #5987。CLA 全綠。未碰 856/858/860/863（該 queue 已由別的 PR #5887/#5888/#5890 佔走）。

## CLA

已簽。既有 PR 的 `cla/google` SUCCESS。CLA 不再擋。

無法自行 merge：`stantheman0128` 對 google-deepmind/formal-conjectures 沒有 merge / auto-merge 權限，main 走 merge queue。

Lean CI（Build Lean project and deploy docs）對 first-time contributor 是 `action_required`：要 **repo maintainer 在 Actions 按 Approve and run workflows**。這不是 CLA，也不是程式錯。本地 `lake --wfail` 已過。

## 已開的 PR（各一題 statement-only）

本地皆以 `lake --wfail build 'FormalConjectures.ErdosProblems.«N»'` 通過（Lean 4.33.1）。沒有證明，只有 `sorry` 陳述。

| PR | 題 | issue | 狀態 / 重點 | 本地 build |
|----|----|-------|-------------|------------|
| https://github.com/google-deepmind/formal-conjectures/pull/5856 | Erdős 784 | #943（good first） | 已解：BoundHolds C ↔ C≤1；排除 1∈A | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5853 | Erdős 896 | #1010 | 已解：max F(A,B) 的 Ford δ Theta | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5854 | Erdős 929 | #1023 | 開放：S(k)≥k^{1-o(1)}；「有素因數 ≤x」不是 x-smooth | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5855 | Erdős 1032 | #1083 | 開放：4-臨界圖 min-degree ≫ n | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5858 | Erdős 875 | #995 | 開放：admissible 子集和集合的 gap 指數 c | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5860 | Erdős 876 | #996 | 開放：subset-sum-free（不是 IsSumFree）gap < n | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5859 | Erdős 1087 | #1287 | 開放：平面 n 點 degenerate 4-sets，f(n)≤n^{3+o(1)} | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5861 | Erdős 935 | #1027 | 三部分：Q₂ 強力部分；ii 已解 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5862 | Erdős 1016 | #1073 | 開放：pancyclic 的 h(n) vs log₂n+log_*n | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5863 | Erdős 1012 | #1070 | 已解（Woodall）：f(k)≤2k+3 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5864 | Erdős 1018 | #1075 | 已解（Kostochka–Pyber）：n^{1+ε} 邊含小非平面子圖 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5865 | Erdős 954 | #1033 | 開放：遞迴 a_k 的 a_i+a_j 解數 = x+O(x^{1/4+o(1)}) | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5866 | Erdős 1122 | #1969 | 開放：additive function 與 log 成長 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5867 | Erdős 1086 | #1286 | 開放：等面積三角形數 g(n) | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5868 | Erdős 1017 | #1074 | 見 PR（statement-only） | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5869 | Erdős 1100 | #1297 | 開放：τ_⊥ / ω；g(k) | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5870 | Erdős 1091 | #1290 | K4-free χ=4 odd cycle diagonals | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5871 | Erdős 1013 | #1071 | 開放：triangle-free χ=k 的 h₃(k) | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5872 | Erdős 960 | #1037 | 開放：ordinary lines f_{r,k}(n) | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5873 | Erdős 976 | #1049 | 開放：F_f(n) 多項式最大素因數 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5874 | Erdős 1143 | #1976 | 開放：F_k(p_i) 區間倍數 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5875 | Erdős 1039 | #1088 | 開放：lemniscate inradius ρ(f) ≫ 1/n | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5876 | Erdős 1066 | #1108 | 開放：min-distance-1 unit graph independence g(n) | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5877 | Erdős 992 | #1057 | 開放：{\alpha x_n} discrepancy | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5878 | Erdős 963 | #1040 | 開放：dissociated subset size f(n)≥⌊log₂ n⌋ | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5879 | Erdős 1045 | #1092 | 見 PR | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5880 | Erdős 983 | #1054 | 開放：f(k,n) 與 2π(√n) | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5881 | Erdős 1005 | #1067 | Farey similarly-ordered window f(n) | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5882 | Erdős 1021 | #1077 | 見 PR | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5883 | Erdős 981 | #1052 | 見 PR | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5884 | Erdős 934 | #1026 | 見 PR | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5885 | Erdős 1033 | #1084 | 見 PR | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5886 | Erdős 911 | #1015 | 開放：size Ramsey $\hat R(G)>f(C)e$ | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5889 | Erdős 919 | #1020 | 開放：χ on ω₂² vs lesser type | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5891 | Erdős 892 | #1009 | 開放：primitive sequence majorants | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5892 | Erdős 1111 | #1964 | 開放：anticomplete sets vs χ, ω | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5893 | Erdős 1089 | #1289 | 開放：g_d(n) distinct distances in R^d | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5896 | Erdős 1132 | #1971 | Lagrange basis polynomial | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5901 | Erdős 917 | #1018 | 開放：k-critical max edges f_k(n) ≫ n² | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5905 | Erdős 1152 | #1982 | 見 PR | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5906 | Erdős 1160 | #1987 | 見 PR | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5902 | Erdős 902 | #1012 | tournament domination f(n) | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5903 | Erdős 915 | #1017 | 見 PR | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5900 | Erdős 878 | #997 | 見 PR | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5904 | Erdős 739 | #4462 | 見 PR | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5910 | Erdős 1162 | #1990 | 開放：|Subgroup S_n| 漸近 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5911 | Erdős 1120 | #1968 | 開放：多項式 sublevel 最短路 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5912 | Erdős 964 | — | 開放：τ(n+1)/τ(n) 在 (0,∞) dense | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5913 | Erdős 1163 | #2020 | 開放：隨機子群 H≤S_n 的 |H| | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5914 | Erdős 977 | — | 已解：P(2^n−1)/n→∞ | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5915 | Erdős 1025 | — | 已解：g(n)=Θ(√n) independent sets for pair maps | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5916 | Erdős 1006 | — | 開放：girth>4 無向圖的無環定向 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5917 | Erdős 1145 | — | A+B 含所有大整數 ⇒ limsup 表示數 ∞ | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5918 | Erdős 980 | — | 開放：∑_{p<x} n_k(p) ∼ c_k x/log x | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5919 | Erdős 978 | — | 多項式 (k−1)-power-free 值；n^4+2 squarefree | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5920 | Erdős 1164 | — | 開放：log R_n ≍ √(log n) 隨機漫步 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5921 | Erdős 1161 | — | 開放：S_n 中 order k 個數何時最大 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5922 | Erdős 1154 | — | 開放：ℝ 的子環/子體的 Hausdorff 維度 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5923 | Erdős 1019 | — | 開放：飽和平面子圖 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5924 | Erdős 1134 | — | 開放：{1} 在 2x+1,3x+1,6x+1 下的下密度 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5925 | Erdős 1046 | — | 開放：連通 lemniscate ⊆ 半徑 2 圓盤 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5927 | Erdős 1123 | — | 開放：密度 0 vs 對數密度 0 的布林代數不同構 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5928 | Erdős 1114 | — | 已解：AP 實根多項式導函數零點間距（Bálint） | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5929 | Erdős 1103 | — | 開放：A+A 無平方因子時 A 的增長 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5930 | Erdős 1042 | — | 已解：transfinite diameter 與 lemniscate 連通分量 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5931 | Erdős 1058 | — | 開放：n!+1 只被 p_k,p_{k+1} 整除的 n 是否有限 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5932 | Erdős 1078 | — | 開放：r-partite min-degree ⇒ K_r | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5933 | Erdős 1166 | — | 已解：Z² 隨機漫步 favourite values 聯集 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5934 | Erdős 1081 | — | 開放：兩個 squarefull 數之和的計數 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5935 | Erdős 1140 | — | 開放：n−2x² 皆為質數的 n 是否無限 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5936 | Erdős 1165 | — | 已解：favourite values |F(n)|=r i.o. | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5937 | Erdős 1149 | — | 開放：gcd(n,⌊n^α⌋)=1 的密度 6/π² | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5938 | Erdős 1099 | — | 開放：liminf h_α(n) ≪_α 1 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5939 | Erdős 1147 | — | 已解：‖α n²‖ 集合不是 2-basis | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5940 | Erdős 1079 | — | 開放：ex(n;K_r) 圖的高密度鄰域 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5941 | Erdős 1124 | — | 開放：等面積正方形與圓的有限全等剖分 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5942 | Erdős 1116 | — | 開放：亞純函數 n(r,a)/n(r,b) limsup | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5943 | Erdős 1180 | — | 開放：模 p 剩餘為短逆元和 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5944 | Erdős 1181 | — | 開放：q(n,log n)<(1-c)(log n)² | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5947 | Erdős 1118 | — | 開放：整函數 E(c) 有限測度與增長 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5948 | Erdős 1053 | — | 開放：k-perfect 是否 k=o(log log n) | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5949 | Erdős 1001 | — | 開放：lim S(N,A,c) 是否存在 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5950 | Erdős 1115 | — | 已解：整函數路徑長度 ℓ(r)≪r 為否 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5952 | Erdős 1069 | — | 已解：k-rich lines ≪ n²/k³ | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5953 | Erdős 1031 | — | 開放：無大平凡誘導子圖 ⇒ 正則誘導子圖 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5954 | Erdős 1183 | — | 開放：單色聯集/交集封閉族 f(n), F(n) | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5955 | Erdős 1184 | — | 開放：f(n,k) 與 Dickman ρ | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5956 | Erdős 994 | — | 開放：幾乎所有 α 對所有可測 E 的等分布 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5957 | Erdős 1182 | — | 開放：R(K₃,G)=2n−1 的邊數 f(n), F(n) | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5958 | Erdős 999 | — | 已解：Khintchine 型 $\sum\phi(q)f(q)/q=\infty$ | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5959 | Erdős 941 | — | 開放：大整數是否為三個 powerful 數之和 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5960 | Erdős 984 | — | 開放：2-著色使單色 AP 長度 ≪_ε a^ε | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5961 | Erdős 947 | — | 開放：無 distinct moduli 的 exact covering | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5962 | Erdős 928 | — | 開放：P(n)<n^α 且 P(n+1)<(n+1)^β 的密度 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5963 | Erdős 989 | — | 已解：圓盤與無限點集的偏差 f(r) 無界 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5964 | Erdős 916 | — | 開放：2n−2 邊含圈上三鄰點的外點 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5965 | Erdős 922 | — | 開放：子圖獨立集 (n−k)/2 ⇒ χ≤k+2 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5966 | Erdős 925 | — | 開放：非 K₃-Ramsey ⇒ α(G)≫n^{1/3+δ} | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5967 | Erdős 880 | — | 開放：k-basis 的有界相異和間距 O(1) | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5968 | Erdős 895 | — | 開放：triangle-free 圖上獨立 a,b,a+b | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5969 | Erdős 910 | — | 已解：R^n 連通集的連通子集 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5970 | Erdős 894 | — | 開放：lacunary 差集的有限著色 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5971 | Erdős 924 | — | 開放：無 K_{l+1} 且 k-Ramsey for K_l | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5972 | Erdős 900 | — | 已解：G(n,cn) 長路徑 f(c)n | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5973 | Erdős 908 | — | 開放：可測差分的連續+可加+零週期分解 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5974 | Erdős 927 | — | 開放：不同 clique 大小數 g(n) | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5975 | Erdős 909 | — | 已解：dim S = dim S² = n 的空間 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5976 | Erdős 874 | — | 開放：admissible k(N)∼2√N | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5977 | Erdős 861 | — | 開放：Sidon 子集個數 A(N)/2^{f(N)} | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5978 | Erdős 877 | — | 開放：極大 sum-free 子集數 f_m(n)=o(2^{n/2}) | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5979 | Erdős 843 | — | 開放：平方數 Ramsey 2-complete | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5980 | Erdős 842 | — | 開放：n 個三角形加 Hamilton 圈的 χ | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5981 | Erdős 926 | — | 開放：ex(n;H_k) ≪ n^{3/2} | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5982 | Erdős 841 | — | 開放：t_n 使 n 乘鄰近積為平方 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5983 | Erdős 819 | — | 開放：|A|=√N 時 |(A+A)∩[1,N]| | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5984 | Erdős 838 | — | 開放：n 點決定的凸子集數 f(n) | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5985 | Erdős 820 | — | 開放：H(n) 與 (k^n−1,l^n−1)=1 | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5986 | Erdős 815 | — | 開放：2n−2 邊且誘導 min-degree≤2 ⇒ C_k | 過 |
| https://github.com/google-deepmind/formal-conjectures/pull/5987 | Erdős 831 | — | 開放：不同半徑的三點圓 h(n) | 過 |

784 的 PR 含 AUTHORS 加入 Po-Han Shih。其餘一檔一 PR。

## 避開、沒做的題

- Erdős 810 / issue #955：已有開放 PR #4090
- Erdős 1117 / issue #1967：已有開放 PR #1808
- Erdős 901 / issue #1011：被批次 PR #5495 佔走（33 題 hypergraph）
- #19 / EFL、#699、Millennium：依指示不做

## 還能接著做的 good-first / 無人認領

good-first + erdos-problems 目前實質空檔很少：810 與 1117 都有開放 PR，784 已由本輪交。

milestone「All open Erdős problems formalized」仍約 264 個 open issue。下一波先 `gh pr list --search N` 再動，較乾淨的候選：

- Erdős 892 / issue #1009（primitive sequence 對 b_n 的充要條件；敘述較含糊）
- Erdős 879 不要搶：已有開放 PR #5302

## ARC Prize 2026

未做。主軸已超過 2 個在飛的 PR，剩餘時間繼續壓 formal-conjectures 而不是離線 agent scaffold。下一步若要做：Kaggle 無外網，只能交純離線程式；目錄應放 `/workspace` 獨立 repo，不要混進 formal-conjectures。

## Erdős #307 弱形式

**無不含 1 的例子。** 含 1 的 Cambie 例子（P={1,5}, Q={2,3} 等）已核對等式成立，但不算。

負結果盒子：
- 1 ∉ P∪Q；P、Q 各自兩兩互質；|P|,|Q|≥2
- 精確 Fraction 算術
- 固定小 P（含 {2,3,5} 目標 30/31，以及 {2,3}、{2,3,7}、{2,3,5,7} 等約 40 組），|Q|≤8、Q 元素無上界的因式搜尋：0 解
- 所有兩兩互質 pair a<b≤400：0 解
- 所有兩兩互質 3-tuples ≤400：約 3.0e6 組，0 解
- 4-tuples 與 5-tuples 的 max_x=200 掃描進行到數千萬組仍 found=0 後中止（超出「找不到就停」）
- 目標分數：P={2,3,5} 時 30/31（Q 必須含 31 的倍數）

沒有可貼 erdosproblems.com/307 Comments 的英文段落。
