#домашнее задание номер 1. онлайн-курсы
#1 задание
основные сущности :
user - польхователи, студенты и преподы
course(курс)- создается преподом
lesson (урок) - из чего состоят курсы
enrollment (запись на курс) - связь между студентом и курсом
review (отзыв) - оставляют студенты

связи:
преподы (user) создают курсы (course), а студенты их смотрят
студенты оставляют отзывы (review) на курс 
курсы (course) состоят из уроков (lesson)

#2 задание
атрибуты
user: user_id, password, email, first_name, last_name
course: course_id, title, teacher_id, description, price, created_at
lesson: lesson_id, course_id, title, content
enrllment: enrllment_id, student_id, course_id, status
review: comment, student_id, review_id

первичные ключи
user: user_id
course: course_id
lesson: lesson_id
enrollment: enrllment_id
review: review_id

внешние ключи 
user: -
course: teacher_id
lesson: course_id
enrollment: student_id
review: student_id, course_id
в моей модели используются суррогатные перичные ключи(serial). для всех таблиц. это значит что у всех сущностей ест ьнеазвисимый ID. поэтому все связи в модели 
неидентифицируеющие. идентифицируеющих связей нет 

<img width="1295" height="682" alt="image" src="https://github.com/user-attachments/assets/7e2b27d5-7e71-4f2f-aea4-f85aa122cb07" />


#4
1) вывести рейтинг курса
2) вывести количество активных студентов на курсе(статус активный, типо ещё не закончили его изучать)
3) самый высокооплачевамый препод
4) вывести список уроков для определенного курса
5) список курсов который ведет один препод

