# The fork
もしもプログラムを書いている途中に分岐を欲した場合は、「if」や「switch」という単語を使う事になるだろう。以下の単語が出現するかもしれない。以下の単語は特に整列された訳ではなく、パラダイムで分割した訳でもない。

- if
- then
- else
- switch
- match
- guard

## IF statement
大抵の言語には、「if」という単語が用意されている。このifという単語は、大抵一つの条件式に対して分岐を作成する。それ以外の場合は、「||」や「&&」と言ったような、論理演算子を用いる事で、複数の条件をまとめる事が出来る。「if」と大抵セットで使われるのが「else」だ。elseは、その条件に当てはまらなかった場合に実行される。

```java:if単体
public class Main {
    public static void main(String[] args) {
        bool i = true;

        if(i == true) {
            System.out.println("i contains true");
        }

        // this program do not say if i variable contains false
    }
}
```

```rust:単一の条件
fn main() {
    let i: bool = true;

    if i == true {
        println!("i contains true");
    } else {
        println!("i contains false");
    }
}
```

```rust:論理演算子使用
fn main() {
    let i: bool = true;
    let j: bool = false;

    if i == true && j == true {
        println!("i and j contains true");
    } else {
        println!("i or j contains false");
    }
}
```

## Then statement
***TODO!!!***
一部の言語では、「then」という単語が使われる事がある。

## switch statement, and match statement in Rust-lang
とある言語には、switch文という構文が用意されていたりする場合がある。しかし、switch文は「if」より採用されている言語は少なかったりする。例えると、C言語にはswitch文が存在するが、Pythonには存在しなかったりする。Rust-langには、switch文の代わりにmatch式が用意されている。大体同じ感じに使えるが、式なので値を返す。そのため、変数の初期化時に使用する事も可能。

```c:switch文
#include <stdio.h>

int main() {
    int i = 2;

    switch(i) {
        case 0:
            printf("i contains 0\n");
            break;

        case 1:
            printf("i contains 1\n");
            break;

        case 2:
            printf("i contains 2\n");
            break;
        
        default:
            printf("i contains anything else");
            break;
    }

    return 0;
}
```

```rust:match式
fn main() {
    let i: i32 = 2;

    let sentence: &str = match i {
        0 => "i contains 0",
        1 => "i contains 1",
        2 => "i contains 2",
        _ => "i contains anything else",
    };

    println!("{}", sentence);
}
```

## The guard
***TODO!!!***