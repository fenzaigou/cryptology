### 数据安全的范畴

- 保密性
- 真实性：消息认证、实体认证
- 数据完整性
- 可用性，可控性，访问控制
- 可审计性：收据和确认，不可否认性



### 安全框架与模型

OSI 安全模型 Open Systems Interconnection 开放式系统互联

- 安全相关的变换算法
- 分发、共享秘密信息的方案
- 指定协议，利用安全变换和秘密信息实现安全服务

网络访问安全模型



### 密码学历史

- 最早记载的加密文字 -- 公元前19世纪古埃及第十二王朝的祭祀碑文

- 最早用于保护信息的密码技术 -- 公元前11世纪武周王时期姜太公发明的阴符（代换加密）、阴书（置乱密码）一合而再离，三发而一知。

- 公元前4世纪斯巴达-波斯战争中的天书（置乱加密）

- 公元前1世纪凯撒密码 C = m + 3 代换密码

- 手工时代：
  手工加解密，代换以技巧为主，辅助少量设备计算
  手工分析，主要靠猜，字频统计分析，密码分析员以语言学家为主

- 20世纪初，进入机电时代，算法复杂度大大增加，安全性大大提高，算法公开，保护密钥，数学家加入密码分析。
  1919年轮转密码机，如 Enigma。

- 计算机时代，密码技术从技巧走向理论，融入大量现代数学理论

  - 1949年 Shannon 的 “The Communication Theory of Secrecy System”
  - 1975年 W.Diffie 和 M.Hellman 提出公开密钥思想
  - 1976年 R.Rivest, A.Shamir 和 L.Adleman 提出RSA算法
  - 1985年 T.EIGamal 提出概率密码系统 EIGamal 方法
  - 当代：混沌密码，量子密码，后量子密码等新兴技术



### 密码学 Cryptology 基本概念

1. Cryptography 密码编码学
2. Cryptanalysis 密码分析学
3. Cryptography Protocol 密码协议



### 密码体制

- 基本要素：密码算法和密钥
- 主要参数
  - 编码的运算类型：代换、置乱
  - 密钥长度
  - 处理明文的方式：序列或分组
  - 加解密的运算复杂度
  - 密文的膨胀
  - 密文错误的传播

S = {P, C, K, E, D}

P: Plaintext C: Ciphertext K: Key E: Encryption D: Description



### 现代密码学的基本原则

- 柯克霍夫原则 （Kerckhoff's Principle
  除密钥以外，密码系统的一切都可以被安全地公开
- 香农箴言（Shannon's maxim）
  敌人了解系统
- 密码系统的安全性取决于对手获取算法和密文之后，分析出密钥或明文的难度。



### 密码体制的安全性

- 无条件安全 Unconditional Security
- 可证明安全 Provable Security
- 计算上安全 Computational Security
- 实际安全 Practical Security



### 密码系统的基本要求

- 遵循柯克霍夫原则，且实际安全
- 加解密算法适用于密钥空间中的所有元素，把弱密钥全部列出，防止泄漏明文信息
- 密钥可随时更改
- 易于实现，使用方便
- 不过分降低通信网络的效率
- 考虑系统实用性，不到使用时不解密数据



### 常关注问题

1. 密钥形式：加解密的密钥是否一致，是否保密
2. 密钥长度
3. 处理明文的方法：按顺序还是一组一组地处理
4. 密文是否唯一
5. 编码过程是否可逆
6. 密文长度是否与明文长度一致
7. 密文容错率：若其中一位传输中出错，会影响多少后续的解密



### 密码技术的应用

- 加密算法的选择

- 通信信道的加密

  - 链路加密 -- 点到点加密
  - 高层连接加密 -- 端到端加密

- 存储数据的加密

  - 硬盘加密

  - 文件加密

    

### 密码体制分类

#### 密钥形式

- 对称密码（Symmetric System, One-Key System, Secret-Key System）
  密钥一致，需保护密钥
- 非对称密码（Asymmetric System, Two-Key System, Public-Key System) 
  加解密的密钥不一致，无法从一个密钥导出另一个密钥，可公开一个密钥

#### 处理明文的方式

- 序列密码体制/流密码体制（Stream Cipher）以bit/byte 为单位进行加解密，同一明文对应不同密文
- 分组密码体制（Block Cipher）以数据块（大于64 bit）为处理单元，同一明文块对应的密文块相同

#### 密文的唯一性分类

- 确定型密码体制（Deterministic cipher）明文和密钥确定后，密文唯一
- 概率型密码体制（Probabilistic Cipher）明文和密钥确定后，密文从密文子集中随机产生，可降低字典攻击的难度

#### 加密算法可逆性

- 可逆变换型密码算法（Reversible Transformation）加解密变换互逆，用于数据的加解密
- 单向函数型密码算法（One-way function）只能正向变换，不可逆，用于不需要解密的场合：口令、验证码



### 常用术语

密码学 Cryptology

密码协议 Cryptographic Protocol

密文 Cryptogram

不可否认性 Non-repudiation

置乱 Transposition, Permutation

乘积密码 Product Cipher

