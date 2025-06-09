https://docs.google.com/document/d/1yf-soLrXXVnJz34jm6lV37lWS5hoxsutKlxjseJfw3o/edit?tab=t.0


задание 1 https://www.loom.com/share/14363ddd0e8c43229e18a9fe8e219385?sid=877a61e0-72d9-4926-ba5e-7a1838d6b728  

задание 2 https://www.loom.com/share/e6b7d8d7728643a7a46a93cb71cd3dfc?sid=c2248908-dddd-4f74-b491-5d0fdadb92e3  

запросы: 
1 - 
SELECT username
FROM users;


2 - 
SELECT users.username,
COUNT(messages.id) AS number_of_sent_messages
FROM users
LEFT JOIN messages ON users.id = messages.from
GROUP BY users.username


3 - 


SELECT users.username, COUNT(messages.id) AS number_of_received_messages
FROM users
LEFT JOIN messages ON users.id = messages.to
GROUP BY users.username
ORDER BY number_of_received_messages DESC


4 - 
SELECT ROUND(1.0 * COUNT(messages.id) / COUNT(DISTINCT users.id), 2) AS avg_sent_messages_per_user
FROM users
LEFT JOIN messages ON users.id = messages.from;


