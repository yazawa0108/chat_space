# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...


**message-table**
|Column|Type|Options|
|------|----|-------|
|body|text|null: false|
|image|string||
|group_id|integer|null: false, foreign_key: true|
|user_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :user
- belongs_to :group

**user-table**
|Column|Type|Options|
|------|----|-------|
|name|text|null: false|
|email|integer|null: false|
|pass-word|integer|null: false|

### Association
- has_many :messages
- belongs_to :groups_users

**group-table**
|Column|Type|Options|
|------|----|-------|
|name|text|null: false|

### Association
- has_many :messages
- belongs_to :groups_users

## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user