liulishuo
=========
实现

有 三个模型

users    表 存放用户信息
  desc 用户描述
  history_count 更新次数缓存
  
follows  表 存储用户关注关系
  user_id  关注者
  follow_id 被关注用户
  
histories 表 存放用户更新的描述
  user_id 发布者
  desc 内容

主要实现
  当用户 更新自己的desc的时候
  保存一份到history记录
  用户通过follow关系 来查看其他用户的 history记录

api的结构

/api/v1/histories
API取得所有用户的描述更新列表（等同于关注了所有用户），按时间降序排列


/api/v1/users
API取得每个用户的描述更新次数
