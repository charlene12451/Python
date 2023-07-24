def find_last_person(n):
    if n < 1:
        return None  
    
    people = list(range(1, n+1))  
    idx = 0  
    
    while len(people) > 1:  
        idx = (idx + 2) % len(people)  
        del people[idx]  

    return people[0] 
    
print(find_last_person(100))
