FizzBuzzKata
============

### Status: http://mebusw.github.io/FizzBuzzKata/

### Here is the problem description:

假如您是一个程序员，要实现一个FizzBuzz的游戏。FizzBuzz是国外小学里老师和孩子们一起玩的游戏。下课前5分钟，老师让孩子们站成一个圈，然后用手指指着第一个孩子，第一个孩子要迅速地说“1”；接着老师快速地指第二个孩子，第二个孩子要迅速说“2”；依次类推，每个被老师指到的孩子要迅速地递增报数。而且，如果孩子遇到3的倍数，就不能说数字，而要说“Fizz”；如果遇到5的倍数，则要说“Buzz”；如果既是3又是5的倍数，则要说“FizzBuzz”。说错或反应慢的孩子就不能再继续游戏。看谁能坚持一直游戏到最后。这是一个很锻炼乘法心算和反应能力的游戏。

您作为程序员，已经按照项目组里的产品需求专家垒君交代的上述需求实现了这个游戏。有一天，垒君找到您，说：“咱们的CEO侨部思在昨天他休4周长假之前跟我说，为了提升咱们这个游戏的趣味性和难度，需要增加一个功能，就是当孩子说Fizz、Buzz或FizzBuzz时，还要同时用手摸自己身体的一个部位。具体摸哪里，侨部思说现在还没想好，他需要时间考虑一下，不过在他休假期间，他说咱们暂时先这样实现：说Fizz同时摸头顶，说Buzz同时摸肩膀，说FizzBuzz同时摸膝盖。等4周他休假回来后，再根据他的最终想法确定该功能。他特意交代，在他休假期间的那次产品发布，不能把这个未完成的功能展示给用户。”

根据您以往的经验，如果用创建分支再合并的方法来完成该功能，会费时费力。为了便于公司正在进行的持续集成和交付，您打算在代码主干上运用特征（Feature Toggle）开关的方法来解决这个问题。

您查阅了下面有关特征开关的一些文章，打算尝试Proxy设计模式来实现特性开关，并试图做到当新功能开发到一半时：1）若特性开关关闭，原有功能和原有测试能够正常运行；2）若特性开关打开，原有功能、原有测试、新功能和新测试都能够正常运行；3）当新功能开发完成并上线前，能方便地移除特性开关。
* Martin Fowler - Feature Toggle: http://martinfowler.com/bliki/FeatureToggle.html
* 路宁 - 特性开关问与答: http://www.luning.name/post/2013-01-17/feature-toggle-faq 
* 孟宇 - 在项目中透明地引入特性开关: http://www.infoq.com/cn/articles/introducing-characteristics-switch-in-project-transparently#rd?sukey=abc050baad029375fe4fc74465447381fc3dfbf0282db3b7a75428d15d780b7bbeb32fbc952743b95e8d2181132f8a8c#3970668-tsina-1-13950-4940258fac58681d93622513463cbd0b