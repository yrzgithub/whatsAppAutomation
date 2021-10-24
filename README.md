import pywhatkit
import keyboard
import time

msg = "double mass"
pywhatkit.sendwhatmsg_instantly("+91 9047665729", "1." + msg)
time.sleep(15)
keyboard.press("enter")
keyboard.release("enter")
j = 1
for i in range(1000):
    if keyboard.is_pressed("shift"):
        break
    keyboard.write("{number}.{msg}".format(number=j, msg=msg))
    time.sleep(0.5)
    keyboard.press("enter")
    keyboard.release("enter")
    j += 1
