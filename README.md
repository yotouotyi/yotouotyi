file = open("marks.csv","r")
a = []
AlM = 0
RuM = 0 
PhM = 0 
HiM = 0
IsM = 0
maxb = 17
count = 0
for line in file:
    a.append(line.split(","))
class Marks:
    N = []
    SN = []
    Al = []
    Ru = []
    Ph = []
    Hi = []
 
M = Marks
for i in range(0, len(a)):
               M.N.append(a[i][0])
               M.SN.append(a[i][1])
               M.Al.append(a[i][2])
               M.Ru.append(a[i][3])
               M.Ph.append(a[i][4])
               M.Hi.append(a[i][5])
 
for v in M.Al:
    AlM += int(v)
print("Средний бал по Алгебре:", AlM/1000)
for v in M.Ru:
    RuM += int(v)
print("Средний бал по Русскому языку:", RuM/1000)
for v in M.Ph:
    PhM += int(v)
print("Средний бал по Физике:", PhM/1000)
for v in M.Hi:
    HiM += int(v)
print("Средний бал по Истории:", HiM/1000)
for c in range (0, len(a)-1):
    st = int(M.Al[c]) + int(M.Ru[c]) + int(M.Ph[c]) + int(M.Hi[c])
    sd = int(M.Al[c+1]) + int(M.Ru[c+1]) + int(M.Ph[c+1]) + int(M.Hi[c+1])
    if sd > st:
        MAX = sd 
    else:
        MAX = st
print("Максимальный бал :", maxb)
print("Люди получившие максимальный бал:")
for l in range (0, len(a)):
    st = int(M.Al[l]) + int(M.Ru[l]) + int(M.Ph[l]) + int(M.Hi[l])
    if st == 17:
        print(a[l])
for l in range (0, len(a)):
    if int(M.Al[l]) == 2 or int(M.Ru[l]) == 2 or int(M.Ph[l]) == 2 or int(M.Hi[l]) == 2:
        count += 1 
print(count)
