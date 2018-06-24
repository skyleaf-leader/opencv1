# opencv1

Anaconda Promptで以下のプログラムを実行

import cv2

# VideoCapture オブジェクトを取得します
capture = cv2.VideoCapture(0)

while(True):
    ret, frame = capture.read()
    cv2.imshow('frame',frame)
    if cv2.waitKey(1) & 0xFF == ord('q'): #frameにfocus, qキータイプでquit
        break

capture.release()
cv2.destroyAllWindows()
