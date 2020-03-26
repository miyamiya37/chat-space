# chat-speace DB設計
## usersテーブル
|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|password|string|null: false|
|username|string|null: false|
### Association
- has_many :chst-messeges
- has_many :chat-groups

## users_chat-groupテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :user
- belongs_to :chat-group

## chat-groupsテーブル
|Column|Type|Options|
|------|----|-------|
|groupname|string|nåull: false|
|user_id|integer|null: false, foreign_key: true|
### Association
- has_many :usera

## chat-massegesテーブル
|Column|Type|Options|
|------|----|-------|
|image|text|null: false|
|text|text|null: false|
|user_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :useraaa