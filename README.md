# Rust logger
## How to add it to my Rust project?
1. Put file `logger.rs` into your project/src folder.
2. Inside of your project's folder run the following command:
```
cargo add log humantime && cargo add colored -F no-color && cargo add fern -F colored
```
3. In main.rs add the following lines:
```
#[macro_use] extern crate log;
pub const CRATE_NAME: &str = module_path!();
mod logger;
```
4. Use logging macros in your project, for example:
```
info!("Info message about variable {}.", var);
debug!("Debug message. Var 1 {}, Var 2 {}.", var1, var2);
trace!("Trace message.");
warn!("Warning!");
error!("Non-fatal error message.");
```
Syntax for logging macros is the same with standard `format!()` macro.