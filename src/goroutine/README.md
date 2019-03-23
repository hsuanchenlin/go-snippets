## mutex1

加上lock與否的差別

```
 go run goroutine/mutex1.go -protecting 0
 go run goroutine/mutex1.go -protecting 1
```
第1行cmd可以看到出現不預期的data

## mutex2

拿掉code 
```cassandraql
hc.counterMu.Lock()
defer hc.counterMu.Unlock()
```
其中之一 會panic

### mutex3
