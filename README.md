#                                                                                                                     二手书销售系统 



## 需求


要求对于不同的使用者，系统的功能与业务逻辑是不完全相同的。对于用户而言，系统主要向用户展示一个友好美观的界面，方便用户浏览各类图书信息，查询图书信息，以及订购图书。而管理员则需要在后台维护这些数据。本系统的主要功能是实现用户购书，用户通过查询书籍信息，找到满意的，将这些书籍添加到购物车，进而完成购买。

系统功能表如下：
![20240604131635](https://github.com/QX7274/Book-sales-management-system/assets/134271611/e216c0e9-faed-4da4-a17b-bfcfd149d48b)

表与表关系如下：
![FU%(9P55 8ASQ4{INQ7ZHSS](https://github.com/QX7274/Book-sales-management-system/assets/134271611/9290c458-28b6-491a-881a-bbfe81ccc67d)

## 功能

- 图书管理功能：

提供一个直观的界面，方便管理员添加、编辑和删除图书信息。
管理员可以输入图书的书名、作者、出版社、ISBN和价格等详细信息，并可为图书分配合适的分类和标签。
记录图书的销售情况和库存数量，以便跟踪库存状况和进行库存管理。

- 顾客管理功能：

提供一个易于使用的界面，方便管理员添加、编辑和删除顾客信息。
管理员可以输入顾客的姓名、地址、联系方式和电子邮箱等详细信息，以便与顾客进行沟通和交流。
跟踪顾客的购买历史和偏好，以个性化顾客服务、推荐和营销。

- 销售管理功能：

允许管理员创建新的销售订单，并记录订单的详细信息，如下单日期、顾客信息和订单状态等。
支持订单状态的更新和取消订单的操作。
生成订单确认和发货通知，以确保及时交付并提供良好的客户体验。

- 订单管理功能：

提供一个界面，方便管理员管理订单信息，包括订单状态的更新和订单日期的记录。
管理员可以查看和编辑订单的详细信息，如顾客信息、订单金额和支付状态等。
支持订单状态的变更和取消订单的操作。

- 库存管理功能：

提供一个界面，方便管理员管理库存信息，包括图书的数量和添加日期等。
管理员可以查看和编辑库存的详细信息，如图书的数量、入库日期和出库记录等。
提供库存报告和警报功能，及时提醒管理员进行库存补充和调整。

- 退货管理功能：

允许管理员处理顾客的退货请求，记录退货的详细信息，如退货日期、顾客信息和退货状态等。
提供一个界面，方便管理员查看和处理退货请求，并更新退货状态和处理结果。

- 会员管理功能：

管理员可以管理顾客的会员信息，包括会员等级、会员积分和会员特权等。
提供一个界面，方便管理员查看和编辑会员信息，并根据会员等级提供相应的优惠和特权。

- 购物车管理功能：

允许顾客将图书添加到购物车，并管理购物车中的项目。
提供一个界面，方便顾客查看和编辑购物车中的图书，并进行结算和下单操作。
支持购物车中图书的数量调整和移除操作。
## 数据库表设计

为了支持上述需求和功能，我们设计了以下数据库表结构：

- `Books`表：存储图书信息，包括书籍的编号、书名、作者、出版社、出版日期、ISBN号和价格等。

- `Customers`表：存储顾客信息，包括顾客的编号、姓名、联系电话、电子邮件和地址等。

- `Admins`表：存储管理员信息，包括管理员的编号、用户名、密码、姓名和联系电话等。

- `Sales`表：记录销售信息，包括销售的编号、销售日期、总销售金额、顾客编号、管理员编号和支付状态等。

- `Orders`表：存储订单信息，包括订单的编号、销售编号、下单日期、顾客编号和管理员编号等。

- `OrderDetails`表：存储订单细节信息，包括订单细节的编号、订单编号、图书编号、数量和价格等。

- `Inventory`表：记录库存信息，包括图书编号、库存数量和最近入库日期等。

- `Returns`表：记录退货信息，包括退货的编号、顾客编号、订单编号、退货日期和退货状态等。

- `Members`表：存储会员信息，包括会员的编号、顾客编号、会员等级和积分等。

- `shopCar`表：存储购物车信息，包括购物车的编号、顾客编号、图书编号、数量和创建日期等。
  
这些表将进一步丰富图书销售管理系统的功能和数据存储，使其更加全面和实用。
