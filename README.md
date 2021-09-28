I've been shilling Solana for too long and I often get asked the same questions about why/where/how to start. 

Below is my best attempt at summarizing quality resources for new devs. In theory, this action-list has everything you need to go from wannabe who never coded Rust to proper Solana hacker. 

Enjoy 🦀⚓🚀

# Why Solana

*Not convinced you should bother? Start here.*

### Read

*I find these 3rd party theses to be most compelling.*

1. [Long post by notboring](https://www.notboring.co/p/solana-summer)
2. [Thesis by multicoin](https://multicoin.capital/2021/05/25/technical-scalability-creates-social-scalability/)
3. [Thesis by sino](https://sinoglobalcap.medium.com/why-we-are-bullish-on-solana-c2be784cfdf6)

### Listen

*I tried to pick a mix of founders shilling their own chain / 3rd party opinions.*

1. [Intro so solana on uncommon core](https://www.youtube.com/watch?v=UVEXSF8uqr0)
2. [Solana founders on upOnly](https://www.youtube.com/watch?v=e8wsw1htJFY)
3. [Unchained - can Solana seize marketshare from Eth](https://unchainedpodcast.com/can-solana-seize-marketshare-from-ethereum-with-serum/)? [oct 2020]
4. [Unchained - could sol displace eth](https://unchainedpodcast.com/sol-is-up-3800-ytd-could-it-eventually-displace-ethereum/)? [aug 2021 - almost a year later]

# Learn rust

*Aight you're excited and ready to jump in. Where do you start? You start with Rust (used for coding "programs" aka smart contracts on Solana.)*

1. [Rust crash course](https://www.udemy.com/course/ultimate-rust-crash-course/) [4h] - excellent, short and to the point intro. 
2. [The official rust lang book](https://doc.rust-lang.org/book/) [1-2d of intense reading] - will teach you syntax and language quirks. 
    1. +++ don't be lazy and do the [exercises for each chapter](https://github.com/rust-lang/rustlings/tree/main/exercises) 
3. [Zero2Prod](https://www.zero2prod.com/) [1-2 wks of study] - will take you from "I get the syntax" to "I get rust as a programming language and where it's strong/weak".

# Learn Solana

*The juicy part.*

1. Read the ["developing" section](https://docs.solana.com/developing/programming-model/overview) of the docs [2-3h] - you will get a lot of questions, but that's ok. Just write them down and you'll be surprised how quickly they get answered as you progress. 
2. Go play with [hello world app](https://github.com/solana-labs/example-helloworld) [2-3h] - rebuilding/tweaking will help your understanding a lot. 
3. Do [paulx's excellent tutorial](https://paulx.dev/blog/2021/01/14/programming-on-solana-an-introduction/) [1-2d]
4. If you feel you need more tutorials:
    1. [Solana transactions in-depth](https://medium.com/@asmiller1989/solana-transactions-in-depth-1f7f7fe06ac2)
    2. Code a smart contract with [David Choi via video tutorials](https://www.youtube.com/watch?v=gA7hFdq2h9Q)
5. Otherwise, if you're ready to progress, it's time to read some actual production program code.
    1. [This library](https://github.com/solana-labs/solana-program-library/) contains code for on-chain programs written by Solana core devs & broader community. It's a gold mine for learning. Pick something you already know (eg token-swap == basically uniswap) → read through it → try adding some features / messing with code. You will learn a lot about architecture and design trade-offs.
7. Now the twist. All of the above showcases "traditional" way of building programs on solana - but there's a simpler / faster way by using [the anchor framework](https://github.com/project-serum/anchor)
    1. Read [this twitter thread](https://twitter.com/armaniferrante/status/1411589629384355840) to understand why it's so powerful
    2. Follow [anchor's onboarding tutorial](https://project-serum.github.io/anchor/getting-started/introduction.html)
8. Build stuff! Fun fun fun. Ideas:
    1. Build a simple blockchain wallet. Personally the first thing I built on Solana was a [tui wallet](https://github.com/ilmoi/degen-wallet) that could do both eth and sol transactions. Taught me a ton about key management and how the two chains compare.
    2. Take something you know on another chain and re-build it on Solana. I picked [fomo3d](https://github.com/ilmoi/solana_fomo3d), which those of you who were around for 2017 craze might remember.
    3. Pick a project in the space that you like and contribute to their repo. [Mango](https://mango.markets/) and [Serum](https://projectserum.com/) are the two that immediately come to mind - both are very keen to fund developers building on top of their protocols.

# Where to get help

*It's ok to be overwhelmed. Here's where you get help.*

- Rust questions
    - Rust community is one of the best I've seen in the dev space. My go to is asking #rust tagged questions on StackOverflow or going to [dedicated rust forums](https://users.rust-lang.org/) if I want to have a bit more of a discussion.
    - Get ready to be amazed! Questions are generally answered within 30min of being asked - that's a totally polar experience to your python/js questions on SO that get 1 reply in 3 days.
    - There's also [Rust discord](https://discord.com/invite/rust-lang-community), if you prefer chats to forums.
- Solana questions
    - Un general all the help is available in discord channels such as:
        - [solana discord](https://discord.com/invite/pquxPsq)
        - [serum discord](https://discord.com/invite/zxPsXcB)
        - [mango discord](https://discord.com/invite/n8c2YhUYmY)
        - etc
    - First thing to do is always Ctrl-F the discord with any keywords you might have from your error. In general, I'd say 50% of the time someone already had that problem and you'll get an instant answer.
    - If that fails, each protocol usually has some sort of `developer questions` channel. Be specific and to the point with your questions (no "hey this is my first post") and don't feel bad  for re-asking ("still looking for answer to this [reply to own previous question]. Anyone might know?). Worst case CC one of the admins who you see frequenting in the chat.
 