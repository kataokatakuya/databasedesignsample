## usersテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false|

###Association
- has_many :members
- has_many :groups


## messagesテーブル

|Column|Type|Options|
|------|----|-------|
|text|text|null: false|
|image|text|

###Association
- belongs_to :member



## membersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

###Association
- belongs_to :group
- belongs_to :user


## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|member_id|integer|null: false, foreign_key: true|

### Association
- has_many :members

