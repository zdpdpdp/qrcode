# QR Code Decoder by Golang

This Project is Developing.

# Plan

1. 动态二值化
2. 提升图片扫描的速度:OK
3. 修复大version时丢失行的bug
4. 容错码纠正数据:OK
5. 数据编码方式
    Numbert
    alphanumeric
    8-bit byte: OK
    Kanji

# Example

    fi, err := os.Open("qrcode.png")
    if !check(err) {
    	return
    }
    defer fi.Close()
    qrmatrix, err := qrcode.Decode(fi)
    if err != nil{
        logger.Println(err.Error())
    }
    logger.Println(qrmatrix.Content)
