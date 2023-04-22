<h1 align="center">CÁC CÂU HỎI PHỎNG VẤN</h1>

## I. Basic

### Câu 1: Java là gì?
**Java** là ngôn ngữ lập trình bậc cao, hướng đối tượng, bảo mật và là 1 platform.

### Câu 2: Thông dịch và biên dịch trong Java?
**Biên dịch (Compile)**: Quá trình biên dịch là quá trình chuyển đổi mã nguồn Java (được viết bằng ngôn ngữ Java) thành mã byte (bytecode) để chạy trên máy ảo Java (JVM). Quá trình biên dịch sẽ tạo ra các tệp class và các tệp khác (ví dụ như tệp jar hoặc war) được sử dụng để triển khai ứng dụng.

**Thông dịch (Interpret)**: Quá trình thông dịch là quá trình chạy các tệp bytecode được tạo ra bởi quá trình biên dịch trên máy ảo Java (JVM). Máy ảo Java sẽ chạy bytecode và dịch nó thành mã máy mà hệ điều hành của máy tính hiểu được. Quá trình thông dịch được sử dụng để thực thi các ứng dụng Java.

### Câu 3: JDK, JRE và JVM là gì?
**JDK (Java Development Kit)**: Là bộ công cụ phát triển Java, bao gồm JDK Compiler, Java Runtime Environment (JRE), Java Debugger và các công cụ khác để phát triển ứng dụng Java. JDK được sử dụng để biên dịch và phát triển ứng dụng Java.

**JRE (Java Runtime Environment)**: Là môi trường chạy ứng dụng Java, bao gồm các thư viện và máy ảo Java (JVM) cần thiết để chạy các ứng dụng Java. JRE không bao gồm các công cụ phát triển, nó chỉ sử dụng để chạy các ứng dụng Java.

**JVM (Java Virtual Machine)**: Là một máy ảo, cung cấp môi trường thực thi cho các ứng dụng Java. JVM được cài đặt trên mỗi máy tính, và nó chạy mã bytecode (mã được biên dịch từ mã nguồn Java) và quản lý bộ nhớ và tài nguyên của ứng dụng.

### Câu 4: Các kiểu dữ liệu và giá trị mặc định của kiểu dữ liệu trong Java.
- **Kiểu nguyên thủy**:
  - **`byte`**: 0
  - **`short`**: 0
  - **`int`**: 0
  - **`long`**: 0L
  - **`float`**: 0.0f
  - **`double`**: 0.0d
  - **`char`**: '\u0000'
  - **`boolean`**: false
- **Kiểu đối tượng**:
  - **`Object`**: null
  - **`String`**: null

### Câu 5: Autoboxing và Unboxing trong Java.
**Autoboxing** và **Unboxing** là quá trình tự động chuyển đổi giá trị giữa kiểu dữ liệu nguyên thủy (primitive type) và kiểu dữ liệu đối tượng tương ứng (wrapper class).

- **Autoboxing** là quá trình tự động chuyển đổi từ kiểu dữ liệu nguyên thủy sang kiểu dữ liệu đối tượng tương ứng. 
```Java
    int a = 10;
    Integer b = a; // autoboxing
```
- **Unboxing** là quá trình tự động chuyển đổi từ kiểu dữ liệu nguyên thủy sang kiểu dữ liệu đối tượng tương ứng. 
```Java
    Integer a = 10;
    int b = a; // unboxing
```

**Lưu ý**: Autoboxing và Unboxing được hỗ trợ từ Java 5 trở lên, giúp cho việc làm việc với kiểu dữ liệu nguyên thủy và kiểu dữ liệu đối tượng trở nên dễ dàng hơn. Tuy nhiên, việc sử dụng quá nhiều autoboxing và unboxing có thể làm tăng đáng kể thời gian thực thi của chương trình, do đó cần cân nhắc khi sử dụng.

### Câu 6: Các mệnh đề `if` trong Java.
1. **if đơn**: được sử dụng để kiểm tra một điều kiện nào đó. Nếu điều kiện đó đúng, thì các câu lệnh bên trong khối `if` sẽ được thực hiện.
```Java
    if (condition) {
        // Block is executed if condition is true
    }
```
2. **if-else**: được sử dụng để kiểm tra một điều kiện. Nếu điều kiện đó đúng, thì các câu lệnh trong khối `if` sẽ được thực hiện. Ngược lại, nếu điều kiện đó sai, thì các câu lệnh trong khối `else` sẽ được thực hiện.
```Java
    if (condition) {
        // Block is executed if condition is true
    } else {
        // Block is executed if condition is false
    }
```
3. **if-else if-else**: được sử dụng khi có nhiều hơn hai điều kiện cần kiểm tra. Các câu lệnh trong khối `if` được thực hiện nếu điều kiện đúng. Nếu điều kiện trong `if` đầu tiên sai, thì điều kiện trong `if-else` tiếp theo sẽ được kiểm tra. Nếu điều kiện đó đúng, thì các câu lệnh trong khối `if-else` sẽ được thực hiện. Nếu không, thì các câu lệnh trong khối `else` cuối cùng sẽ được thực hiện.
```Java
    if (condition1) {
        // Block is executed if condition1 is true
    } else if (condition2) {
        // Block is executed if condition1 is false and condition2 is true
    } else {
        // Block is executed if the above 2 conditions are false
    }
```
4. **Nested if (if lồng nhau)**: mệnh đề nested `if` được sử dụng khi một mệnh đề `if` được nhúng trong một khối `if` hoặc `else` của một mệnh đề `if` khác.
```Java
    if (condition1) {
        // Block is executed if condition1 is true
    } else {
        // Block is executed if condition1 is false
        if (condition2) {
            // Block is executed if condition2 is true
        } else {
            // Block is executed if condition2 is false
        }
    } 
```
### Câu 7: `Switch-case` trong Java?
**`Switch-case`** là một cấu trúc điều khiển lựa chọn trong Java, cho phép bạn kiểm tra giá trị của biến và thực hiện hành động tương ứng với giá trị đó.
```Java
    switch(variable) {
        case value1:
            // code to be executed if variable == value1
            break;
        case value2:
            // code to be executed if variable == value2
            break;
        ...
        default:
            // code to be executed if variable is different from all values
}
```
Khi chạy, `switch-case` sẽ kiểm tra giá trị của `variable` và thực hiện hành động tương ứng với giá trị đó. Nếu không có giá trị nào phù hợp, `switch-case` sẽ thực hiện hành động ở trường hợp `default`.
*** Ví dụ:
```Java
    int day = 3;
    switch(day) {
        case 1:
            System.out.println("Monday");
            break;
        case 2:
            System.out.println("Tuesday");
            break;
        case 3:
            System.out.println("Wednesday");
            break;
        case 4:
            System.out.println("Thursday");
            break;
        case 5:
            System.out.println("Friday");
            break;
        default:
            System.out.println("Weekend");
    }
```
```Console
// Kết quả sẽ là "Wednesday", vì day có giá trị là 3.
Wednesday
```

### Câu 8: Cách cách khai báo mảng trong Java?
**1. Khai báo mảng có độ dài có định.**
>Khai báo mảng 1 chiều
```Java
    DataType[] array_name = new DataType[length];
    // Or
    DataType array_name[] = new DataType[length];
```    
>Khai báo mảng đa chiều
```Java
    DataType[][] array_name = new DataType[rowSize][columnSize];
    // Or
    DataType array_name[][] = new DataType[rowSize][columnSize];
```

*** Ví dụ:
```Java
    // One-dimensional array
    int[] numbers = new int[5];
    // Or
    int numbers[] = new String[5];

    // Multidimensional array
    int[][] numbers = new int[5][5];
    // Or
    int numbers[][] = new int[5][5];

```

**2. Khai báo mảng với các giá trị khởi tạo.**
>Khai báo mảng 1 chiều
```Java
    DataType[] array_name = {value1, value2,...};
    // Or
    DataType array_name[] = {value1, value2,...};
```
>Khai báo mảng đa chiều
```Java
    DataType[][] array_name = {{value1, value2,...}, {value3, value4,...}};
    // Or
    DataType array_name[][] = {{value1, value2,...}, {value3, value4,...}};
```

*** Ví dụ:
```Java
    // One-dimensional array
    int[] numbers = {1, 2, 3};
    // Or
    int numbers[] = {1, 2, 3};
    
    // Multidimensional array
    int[][] numbers = {{1, 2, 3}, {4, 5, 6}};
    // Or
    int numbers[][] = {{1, 2, 3}, {4, 5, 6}};
```

**3. Khai báo mảng bằng cách sử dụng toán tử `new` .**
>Khai báo mảng 1 chiều
```Java
    DataType[] array_name = new DataType[]{value1, value2,...};
    // Or
    DataType array_name[] = new DataType[]{value1, value2,...};
```    
>Khai báo mảng đa chiều
```Java
    DataType[][] array_name = new DataType[][]{{value1, value2,...}, {value3, value4,...},...};
    // Or
    DataType array_name[][] = new DataType[][]{{value1, value2,...}, {value3, value4,...},...};
```

*** Ví dụ:
```Java
    // One-dimensional array
    int[] numbers = new int[]{1, 2, 3};
    // Or
    int numbers[] = new int[]{1, 2, 3};
    
    // Multidimensional array
    int[][] numbers = new int[][]{{1, 2, 3}, {4, 5, 6}};
    // Or
    int numbers[][] = new int[][]{{1, 2, 3}, {4, 5, 6}};
```

**Lưu ý**:
 - Các phần tử của mảng đa chiều phải cùng kiểu dữ liệu.
 - Khi khai báo mảng đa chiều bằng từ khóa new, số lượng phần tử của mỗi chiều phải được xác định trước.
 - Khi khai báo mảng đa chiều bằng giá trị khởi tạo, số lượng phần tử của mỗi chiều có thể khác nhau.
 - Các phần tử của mảng đa chiều có thể truy cập thông qua chỉ số của từng chiều.
 - Khi truy cập phần tử của mảng đa chiều, cần kiểm tra rằng chỉ số của từng chiều không vượt quá kích thước của mảng. Việc truy cập vượt quá kích thước của mảng sẽ gây ra lỗi `ArrayIndexOutOfBoundsException`.
### Câu 9: Loop (Vòng lặp) trong Java?

**1. `for` loop**: là một vòng lặp có điều kiện, được sử dụng khi biết trước số lần lặp.
```Java
    for (initialization; condition; increment/decrement) {
    // statements
    }
```
- **Trong đó**:
  - **Initialization**: phần khởi tạo, thường là gán giá trị ban đầu cho biến đếm.
  - **Condition**: điều kiện để vòng lặp tiếp tục.
  - **Increment/decrement**: bước nhảy của biến đếm sau mỗi lần lặp.

*** Ví dụ
```Java
    for (int i = 0; i < 5; i++) {
        System.out.println("i = " + i);
    }
```
```Console
// Kết quả:
i = 0
i = 1
i = 2
i = 3
i = 4
```

**2. `for-each` loop**: là một cú pháp ngắn gọn để lặp qua tất cả các phần tử trong một collection hoặc một mảng trong Java. `for-each` loop còn được gọi là enhanced for loop.
```Java
    for (type variable : array/collection) {
    // Code block to be executed
    }
```
- **Trong đó**:
  - **type**: là kiểu dữ liệu của phần tử trong mảng hoặc collection.
  - **variable**: là biến để lưu giá trị của từng phần tử khi lặp qua.
  - **array/collection**: là mảng hoặc collection để lặp qua.
```Java
    int[] numbers = {1, 2, 3, 4, 5};

    for (int number : numbers) {
        System.out.println(number);
    }
```
```Console
// Kết quả:
1
2
3
4
5
```

**3. `while` loop**: là một vòng lặp không có số lần lặp cụ thể, được sử dụng khi số lần lặp không biết trước hoặc phụ thuộc vào một điều kiện nào đó.
```Java
    while (condition) {
        // statements
    }
```
- **Trong đó**: 
  - **Condition**: điều kiện để vòng lặp tiếp tục.
```Java
    int i = 0;
    while (i < 5) {
        System.out.println("i = " + i);
        i++;
    }
```
```Console
// Kết quả:
i = 0
i = 1
i = 2
i = 3
i = 4
```

**4. `do-while` loop**: là một vòng lặp tương tự như `while` loop, nhưng sẽ thực hiện ít nhất một lần kể cả khi điều kiện không thỏa mãn.
```Java
    do {
    // statements
    } while (condition);
```
- **Trong đó**: 
  - **Statements**: đoạn mã thực hiện trong vòng lặp.
  - **Condition**: điều kiện để vòng lặp tiếp tục.
```Java
    int i = 0;
    do {
        System.out.println("i = " + i);
        i++;
    } while (i < 5);
```
```Console
// Kết quả:
i = 0
i = 1
i = 2
i = 3
i = 4
```

### Câu 10: OOP là gì?

**OOP (Object oriented programming - Lập trình hướng đối tượng)** là kỹ thuật lập trình cho phép lập trình viên trừu tượng hóa các đối tượng thực tế thành các đối tượng trong code.

### Câu11: Các tính chất trong OOP.
---
## II. Junior
```Java
    System.out.println("=>" + variable);
```
---

## III. Middle

---

## IV. Senior

---