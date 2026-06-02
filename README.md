UPDATE users SET email = CASE                                                
    WHEN id % 3 = 0 THEN 'hongjx0321+patient' || id || '@gmail.com'            
    WHEN id % 3 = 1 THEN 'wygen123+patient' || id || '@gmail.com'              
    WHEN id % 3 = 2 THEN 'dummyusersigningin01+patient' || id || '@gmail.com'  
   END                                                                          
   WHERE id IN (SELECT user_id FROM patients);