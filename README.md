# i-Os
class Student:
  def __init__(self, name, year):
    self.name=name
    self.year=year
    self.grades=[]  
  def add_grade(self, grade):
    if type(grade) is Grade:
      self.grades.append(grade)  
roger=Student("Roger van der Weyden", 10)
sandro=Student("Sandro Botticelli", 12)
pieter=Student("Pieter Bruegel the Elder",8)
class Grade:
  minimum_passing=65
  def __init__(self, score):
    self.score=score
  def is_passing(self, score):
    return score>minimum_passing
Grade(100)
pieter.add_grade(Grade(100))
#print(pieter.is_passing(Grade(100)))
print(pieter.grades[0])
pieter.add_grade(Grade(30))
print(pieter)
