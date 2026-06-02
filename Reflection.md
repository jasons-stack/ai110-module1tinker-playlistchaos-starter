# Tech Fellow Reflection – Week 1: Playlist Chaos

The main concept students needed to understand in this activity is how to 
trace broken logic in existing code by forming expectations first and then 
comparing them against what the app actually does. Students are most likely 
to get stuck on the search bug because the condition `value in q` is valid 
Python that runs without any errors, making it hard to spot without carefully 
walking through a specific example by hand. AI tools were helpful for 
explaining what individual functions were doing and suggesting cleaner ways 
to structure the classification logic in `classify_song`, but they could be 
misleading when analyzing the stats bugs since the errors are subtle enough 
that an AI might describe the broken code as if it were correct. The 
`random_choice_or_none` function is another area where AI could mislead 
students, since it looks fine at a glance and an AI assistant likely won't 
flag the empty list crash unless the student asks about edge cases specifically. 
To guide a student toward the search fix without giving it away, I would ask 
them to trace through a specific example: 

"if the artist is 'AC/DC' and you 
search 'ac', what does `value` equal, what does `q` equal, and what does 
`value in q` actually evaluate to?"