

```c#
var query = db.Students
    .Where(s => s.Age > 18);
    
    
    
    
    call: Querable.where
	    |-Source:DbSet Students
	    |-Predicate
		    |-Lambda
			    |-GreaterThan
				    |-s.Age
					|18






var query = db.Students
    .Where(s => s.Age > 18)
    .OrderBy(s => s.Name);
    
    
    
    
    call: Querable.where
	    |-Source:DbSet Students
	    |-Predicate
		    |-Lambda
			    |-GreaterThan
				    |-s.Age
					|18
		|-KeySelector:s.Name




var query = db.Students
    .Where(s => s.Age > 18)
    .OrderBy(s => s.Name)
    .Select(s => new { s.Id, s.Name });
    
    
    
    
    call: Querable.where
	    |-Source:DbSet Students
	    |-Predicate
		    |-Lambda
			    |-GreaterThan
				    |-s.Age
					|18
		|-KeySelector:s.Name













var query = db.Orders  
.Where(o => o.Total > 1000);




Queryable.Where(  
db.Orders,  
o => o.Total > 1000  
)
```

![[Pasted image 20260513165021.png]]