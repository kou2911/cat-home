# テーブル設計

## usersテーブル

| Column             | Type   | Option                      |
| ------------------ | -----  | ------------------------    |
| email              | string | null: false, unique: true   |
| encrypted_password | string | null: false                 |
| nickname           | string | null: false                 |
| last_name          | string | null: false                 |
| first_name         | string | null: false                 |
| last_name_reading  | string | null: false                 |
| first_name_reading | string | null: false                 |
| birthday           | date   | null: false                 |

## Association

- has_many  :cats

## catsテーブル

| Column             | Type      | Option                          |
| -----------------  | --------  | ------------------------------  |
| cat_name           | string    | null: false                     |
| feature            | text      | null: false                     |
| age_id             | integer   | null: false                     |
| place_id           | integer   | null: false                     |
| vaccine_id         | integer   | null: false                     |
| castration_id      | integer   | null: false                     |
| sickness_id        | integer   | null: false                     |
| memo               | text      |                                 |
| contact_address    | string    | null: false                     |
| user               | reference | null: false, foreign_key: true  |

## Association

- has_many_attached :images
- belongs_to  :user
