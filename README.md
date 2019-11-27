# Rust_practice

*Ce Repository contient tout les exercices et TP que j'ai réalisé en Rust. J'ai principalement suivi la documentation de Rust et le cours en ligne "Rust Fondamentals*.


This repository contains all my Rust exercices and practice. I mainly follow the official Rust documentation and the "Rust Fondamentals" course.


## How to use Rust / Comment débuter avec Rust :

*Ce Repository contient des fichiers provenant de Rust et Cargo. Pour utiliser Rust, suivez simplement les instruction dans la documentation officielle (Pas traduite en Français à l'heure actuelle)*


This repository contains Rust and Cargo files. In order to run them and start using Rust, just follow these simple steps of the official Rust documentation here :


> https://doc.rust-lang.org/cargo/getting-started/index.html


*J'ai créé ce Repository car la majorité de mes collègues et amis n'avaient jamais entendu parler de ce langage, vous pouvez en apprendre un peu plus à ce sujet [ici.](https://fr.wikipedia.org/wiki/Rust_(langage))*


I made this repository because most of my coworkers or friends have never even heard of Rust.
You can learn more about it [here.](https://en.wikipedia.org/wiki/Rust_%28programming_language%29)

## [First Steps with Cargo](https://doc.rust-lang.org/cargo/getting-started/first-steps.html#first-steps-with-cargo)


*Pour créer un nouveau package avec Cargo, utilisez la commande  `cargo new`:*

To start a new package with Cargo, use `cargo new`:

```console
$ cargo new hello_world
```
*Voyons ce que Cargo à généré pour nous après cette commande :*

Let’s check out what Cargo has generated for us:

```console
$ cd hello_world
$ tree .
.
├── Cargo.toml
└── src
    └── main.rs

1 directory, 2 files
```
*Voila tout ce qu'il nous faut pour démarrer. Regardez `Cargo.toml`: *

This is all we need to get started. First, let’s check out `Cargo.toml`:

```
[package]
name = "hello_world"
version = "0.1.0"
authors = ["Your Name <you@example.com>"]
edition = "2018"

[dependencies]
```
*Cela s'appelle le **manifeste**, et il contient toutes les métadonnées dont Cargo à besoin pour compiler votre package.*

This is called a **manifest**, and it contains all of the metadata that Cargo needs to compile your package.

*Voici le contenu de `src/main.rs`:*

Here’s what’s in `src/main.rs`:


```rust
fn main() {
    println!("Hello, world!");
}
```

*Cargo à généré automatiquement un Hello World, compilez le :*


Cargo generated a “hello world” for us. Let’s compile it:

```console
$ cargo build
   Compiling hello_world v0.1.0 (file:///path/to/package/hello_world)
```

And then run it :

*Puis lancez le avec la commande :*

```console
$ ./target/debug/hello_world
Hello, world!
```

We can also use `cargo run` to compile and then run it, all in one step:

*Une méthode plus simple :  `cargo run` permet de compiler et lancer le code, le tout en une seule commande.* 

```console
$ cargo run
     Fresh hello_world v0.1.0 (file:///path/to/package/hello_world)
   Running `target/hello_world`
Hello, world!
```
