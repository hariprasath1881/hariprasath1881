def algu(text,key):
    result=""
    for char in text:
     if char == ' ':
        result = result + char
     elif(char.isupper()):
        result=result+chr((ord(char)+key-65)%26+65)
     else:
        result=result+chr((ord(char)+key-97)%26+97)

    return result
text=input("ENTER YOUR TEXT : ")
key=int(input("ENTER THE KEY : "))

print("after encryption :",algu(text,key))
