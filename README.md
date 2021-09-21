## Workspace重點：
* 所有工作空間會共用同一個target跟Cargo.lock
* 庫之間彼此的依賴要手動加在各自的Cargo.toml下
* 外部依賴也要手動加在各自的[dependencies]下
* 對於外部依賴，即便在[dependencies]指定了不同版本，cargo也會讓他們依賴同一版本
* 發佈到crates.io時要到各目錄下分別publish

#### cargo run 加上 -p 參數
`$ cargo run -p adder`

#### Test會全局run一次
`$ cargo test`

#### Test單一庫
`$ cargo test -p add_one`