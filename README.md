string = (str(input("Input text:\n")))

trans = {44:None, 59:None, 34:None}
string = string.translate(trans)

string_split = string.split('. ')
string1 = string_split[0]

string2 = string1.split(' ')
mylist = []
mylist2 = []

for i in string2:
    temp = len(i)
    mylist.append(temp)

j = -1
for i in string_split:
    if i == string_split[0]:
        continue
    j += 1
    string3 = i.split(' ')
    num = (int(mylist[j])) - 1
    temp = string3[num]
    mylist2.append(temp)

result = ' '
mylist2[0] = mylist2[0].title()
result = str(result.join(mylist2))
print(result + '.')
