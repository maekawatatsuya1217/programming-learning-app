# テーブル設計

##user

| Column     | Type   | Options  |
| ---------- | ------ | -------- |
| email      | string | NOT NULL |
| password   | string | NOT NULL |
| name       | string | NOT NULL |
| profile    | text   | NOT NULL |

- has_many :calendars


##calendars

| Column  | Type       | Options                       |
| ------- | ---------- | ----------------------------- |
| content | string     |                               |
| date    | datetime   | null: false                   |
| user    | references | null: false, foreign_key: tru |


- belongs_to :user

##blog

| Column  | Type       | Options  |
| ------- | ---------- | -------- |
| title   | string     | NOT NULL |
| catch   | string     | NOT NULL |
| article | text       | NOT NULL |
| user    | references |          |

belongs_to :user