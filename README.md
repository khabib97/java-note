# java-note
try to gather java knowledge base

## 1. nextLine() issue
If you use the nextLine() method immediately following the nextInt() method, recall that nextInt() reads integer tokens; because of this, the last newline character for that line of integer input is still queued in the input buffer and the next nextLine() will be reading the remainder of the integer line (which is empty).

```
int N = scanner.nextInt();
scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");
```
