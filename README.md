# BCE-Service

A python lib to call Baidu BCE API.

## Baidu OCR API

An great API to recognize text (Enghlish or Simple Chinese) in an image (only support jpg/png format currently).

### Usage:

Initialize an BceOCRAPI object:    

    ocr = BceOCRAPI(access_token, secret_token)

Encode the image data with base64 lib    

    import base64
    with open('image.jpg', 'rb') as f:
        content = f.read()
        content = base64.b64encode(content)

Recognize all the text in the image:

    result = ocr.get_ocr_text(content, language='CHN_ENG')

Recognize a line of text in the image:

    result = ocr.get_ocr_line(content, language='CHN_ENG')

Recognize a character in the image:

    result = ocr.get_ocr_char(content, language='CHN_ENG')


A sample implementation pls visit [Cloudesk.top OCR](http://cloudesk.duapp.com/ocr/)

Pls use this invite code `QzWgtyK7ND` to register as an member of cloudesk. 

Enjoy and cheers!
