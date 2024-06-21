# Security Papers in WebAssembly
This repository contains a curated collection of research papers on security topics related to WebAssembly, sourced from top-tier Software Engineering and Security conferences. The aim is to ensure comprehensive coverage of significant publications in the field.

Organizing a literature review for my thesis has been challenging. To streamline the process, I've created this repository to categorize relevant papers. Special thanks to [Jianing](https://wasm.jianing.wang/#/papers) for providing the initial list of papers.

## Table of contents
- [Security-Papers-in-WebAssembly](#security-papers-in-webassembly)
	- [Table of contents](#table-of-contents)
	- [SoK, Empirical Study, and Survey](sok,-empirical-study,-and-survey)
	- [WASM Binary](#wasm-binary)
	  - [Protection and Hardening](#protection-and-hardening)
	  - [Fuzzing (WASM Binary)](#fuzzing)
	  - [Dynamic Analysis (Other than fuzzing)](dynamic-analysis)
	  - [SAST (WASM Binary)](#sast)
	  - [Obfuscation and Detection Evasion](#obfuscation-and-detection-evasion)
	  - [Reverse Engineering](#reverse-engineering)
	  - [Rewriting](#rewriting)
	  - [Porting Issues](#porting-issues)
	- [WASM Runtime and Compiler](#wasm-runtime-and-compiler)
 		- [SFI](#sfi)
 		- [Fuzzing and Differential Testing (WASM Runtime)](#fuzzing-and-differential-testing)
 		- [SAST (WASM Runtime)](#sast-for-runtimes)
		- [Efficiency](#efficiency)
	- [Applications in Security](#applications-in-security)

## SoK, Empirical Study, and Survey
- Harnes, Håkon, and Donn Morrison. ["SoK: Analysis Techniques for WebAssembly."](https://www.mdpi.com/1999-5903/16/3/84/pdf), Future Internet, 2024.
- `Runtime` Wang, Yue, et al. ["A Comprehensive Study of WebAssembly Runtime Bugs."](https://ieeexplore.ieee.org/abstract/document/10123536), SANER, 2023.
- Hilbig, Aaron, Daniel Lehmann, and Michael Pradel. ["An empirical study of real-world webassembly binaries: Security, languages, use cases."](https://www.software-lab.org/publications/www2021.pdf), WWW, 2021.
- `Compiler` Romano, Alan, et al. ["An empirical study of bugs in webassembly compilers."](https://par.nsf.gov/servlets/purl/10312862), ASE, 2021.
- Lehmann, Daniel, Johannes Kinder, and Michael Pradel. ["Everything old is new again: Binary security of WebAssembly."](https://www.usenix.org/system/files/sec20-lehmann.pdf), USENIX Security, 2020.
- Musch, Marius, et al. ["New Kid on the Web: A Study on the Prevalence of WebAssembly in the Wild."](https://intellisec.org/pubs/2019a-dimva.pdf), DIMVA, 2019.

## WASM Binary
  
### Protection and Hardening
- Cabrera-Arteaga, Javier, et al. ["Wasm-Mutate: Fast and effective binary diversification for WebAssembly."](https://www.sciencedirect.com/science/article/pii/S0167404824000324), Computers & Security, 2024.
- Rao, Xiaojia, et al. ["Iris-wasm: Robust and modular verification of webassembly programs."](https://dl.acm.org/doi/pdf/10.1145/3591265), PLDI, 2023.
- Stiévenart, Quentin, Coen De Roover, and Mohammad Ghafari. ["The security risk of lacking compiler protection in WebAssembly."](https://arxiv.org/pdf/2111.01421), QRS, 2021.
- Narayan, Shravan, et al. ["Swivel: Hardening WebAssembly against spectre."](https://www.usenix.org/system/files/sec21-narayan.pdf), USENIX Security, 2021.
- Watt, Conrad, et al. ["Ct-wasm: type-driven secure cryptography for the web ecosystem."](https://dl.acm.org/doi/pdf/10.1145/3290390), POPL, 2019.
- Watt, Conrad, Andreas Rossberg, and Jean Pichon-Pharabod. ["Weakening webassembly."](https://dl.acm.org/doi/pdf/10.1145/3360559), OOPSLA, 2019.
- Sun, Jian, et al. ["SELWasm: A Code Protection Mechanism for WebAssembly."](https://ieeexplore.ieee.org/abstract/document/9047432), ISPA, 2019.


### Fuzzing
- Lehmann, Daniel, Martin Toldam Torp, and Michael Pradel. ["Fuzzm: Finding memory bugs through binary-only instrumentation and fuzzing of webassembly."](https://arxiv.org/pdf/2110.15433), arXiv preprint, 2021.

### Dynamic Analysis 
- Lehmann, Daniel, and Michael Pradel. ["Wasabi: A framework for dynamically analyzing webassembly."](https://arxiv.org/pdf/1808.10652), ASPLOS, 2019.
- Fu, William, Raymond Lin, and Daniel Inge. ["Taintassembly: Taint-based information flow control tracking for webassembly."](https://arxiv.org/pdf/1802.01050), arXiv preprint, 2018.

### SAST
- Chen, Weimin, et al. ["Wasai: uncovering vulnerabilities in wasm smart contracts."](https://dl.acm.org/doi/pdf/10.1145/3533767.3534218), ISSTA, 2022.
- Brito, Tiago, et al. ["Wasmati: An efficient static vulnerability scanner for WebAssembly."](https://www.sciencedirect.com/science/article/pii/S0167404822001407) Computers & Security, 2022.
- He, Ningyu, et al. ["EOSAFE: Security analysis of EOSIO smart contracts."](https://www.usenix.org/system/files/sec21-he-ningyu.pdf), USENIX Security, 2021.
- Lopes, Pedro Daniel Rogeiro. ["Discovering vulnerabilities in webassembly with code property graphs."](https://syssec.dpss.inesc-id.pt/projects/tr-wasmati.pdf), Técnico Lisboa, 2021.
- Stiévenart, Quentin, and Coen De Roover. ["Compositional information flow analysis for WebAssembly programs."](https://cris.vub.be/ws/files/75991494/informationflow_copyright.pdf), SCAM, 2020.

### Obfuscation and Detection Evasion
- Harnes H, Morrison D. ["Cryptic Bytes: WebAssembly Obfuscation for Evading Cryptojacking Detection"](https://arxiv.org/pdf/2403.15197), arXiv preprint, 2024.
- Cao, Shangtong, et al. ["WASMixer: Binary Obfuscation for WebAssembly"](https://arxiv.org/pdf/2308.03123), ESORICS, 2024
- Cabrera-Arteaga, Javier, et al. ["WebAssembly diversification for malware evasion."](https://www.sciencedirect.com/science/article/pii/S0167404823002067), Computers & Security, 2023.
- Loose, Nils, et al. ["Madvex: Instrumentation-Based Adversarial Attacks on Machine Learning Malware Detection."](https://arxiv.org/pdf/2305.02559), DIMVA, 2023.
- Bhansali, Shrenik, et al. ["A first look at code obfuscation for webassembly."](https://dl.acm.org/doi/pdf/10.1145/3507657.3528560), WiSec, 2022.
  
### Malware Detection
- Xia, Yifan, et al. ["Static Semantics Reconstruction for Enhancing JavaScript-WebAssembly Multilingual Malware Detection."](https://arxiv.org/pdf/2310.17304), ESORICS, 2023.
- Naseem, Faraz Naseem, et al. ["MINOS: A Lightweight Real-Time Cryptojacking Detection System."](https://www.researchgate.net/profile/Ahmet-Aris/publication/349109071_MINOS_A_Lightweight_Real-Time_Cryptojacking_Detection_System/links/61488e123c6cb310697fba33/MINOS-A-Lightweight-Real-Time-Cryptojacking-Detection-System.pdf), NDSS, 2021.

### Reverse Engineering
- `WasmRev` Huang H, Zhao J. ["Multi-modal Learning for WebAssembly Reverse Engineering"](https://arxiv.org/pdf/2404.03171), ISSTA, 2024.
- Lehmann, Daniel, and Michael Pradel. ["Finding the dwarf: recovering precise types from WebAssembly binaries."](https://www.software-lab.org/publications/pldi2022.pdf), PLDI, 2022.
- Lehmann, Daniel, et al. ["That’s a Tough Call: Studying the Challenges of Call Graph Construction for WebAssembly."](https://dl.acm.org/doi/abs/10.1145/3597926.3598104), ISSTA, 2023.
- Romano, Alan, and Weihang Wang. ["Automated WebAssembly Function Purpose Identification With Semantics-Aware Analysis."](https://dl.acm.org/doi/pdf/10.1145/3543507.3583235), WWW, 2023.


### Slicing
- Stiévenart, Quentin, David W. Binkley, and Coen De Roover. ["Static stack-preserving intra-procedural slicing of webassembly binaries."](http://soft.vub.ac.be/Publications/2022/vub-tr-soft-22-04.pdf), ICSE, 2022.

### Rewriting
- Cao, Shangtong, et al. ["A General Static Binary Rewriting Framework for WebAssembly."](https://arxiv.org/pdf/2305.01454), SAS, 2023.

### Porting Issues
- Stiévenart, Quentin, Coen De Roover, and Mohammad Ghafari. ["Security risks of porting c programs to WebAssembly."](https://arxiv.org/pdf/2112.11745), SAC. 2022.


## WASM Runtime and Compiler

### SFI
- VanHattum, Alexa, et al. ["Lightweight, Modular Verification for WebAssembly-to-Native Instruction Selection."](https://cs.wellesley.edu/~avh/veri-isle-preprint.pdf), ASPLOS, 2024.
- `PKUWA` `MPK` `Runtime` Lei, Hanwen, et al. ["Put Your Memory in Order: Efficient Domain-based Memory Isolation for WASM Applications."](https://dl.acm.org/doi/pdf/10.1145/3576915.3623205), CCS, 2023.
- `Runtime` Johnson, Evan, et al. ["WaVe: a verifiably secure WebAssembly sandboxing runtime."](https://cseweb.ucsd.edu/~dstefan/pubs/johnson:2023:wave.pdf), S&P, 2023.
- Kolosick, Matthew, et al. ["Isolation without taxation: near-zero-cost transitions for webassembly and sfi."](https://dl.acm.org/doi/pdf/10.1145/3498688), POPL, 2022.
- Bosamiya, Jay, Wen Shih Lim, and Bryan Parno. ["Provably-Safe Multilingual Software Sandboxing using WebAssembly."](https://www.usenix.org/system/files/sec22-bosamiya.pdf), USENIX Security, 2022.
- Johnson, Evan, et al. ["Доверяй, но проверяй: SFI safety for native-compiled Wasm."](https://par.nsf.gov/servlets/purl/10228509), NDSS, 2021.
- Narayan, Shravan, et al. ["Retrofitting fine grain isolation in the Firefox renderer."](https://www.usenix.org/system/files/sec20-narayan.pdf), USENIX Security, 2020.

### Fuzzing and Differential Testing
- Han, Jideng, et al. ["ESFuzzer: An Efficient Way to Fuzz WebAssembly Interpreter."](https://www.mdpi.com/2079-9292/13/8/1498), Electronics, 2024
- `Efficiency` `WarpDif` Jiang, Shuyao, et al. ["Revealing Performance Issues in Server-side WebAssembly Runtimes via Differential Testing."](https://arxiv.org/pdf/2309.12167), ASE, 2023.
- Zhou, Shiyao, et al. ["WADIFF: A Differential Testing Framework for WebAssembly Runtimes."](https://ieeexplore.ieee.org/abstract/document/10298359), ASE, 2023.
- Cao, Shangtong, et al. ["WRTester: Differential Testing of WebAssembly Runtimes via Semantic-aware Binary Generation."](https://arxiv.org/html/2312.10456v1), arXiv preprint, 2023.
- Jiang, Bo, et al. ["Wasmfuzzer: A fuzzer for webassembly virtual machines."](https://ksiresearch.org/seke/seke22paper/paper165.pdf), SEKE, 2022.


### SAST for Runtimes
- Zhang, Yixuan, et al. ["Characterizing and detecting webassembly runtime bugs."](https://arxiv.org/pdf/2301.12102), TSEM, 2023.

### Efficiency
- `WasmFX` Phipps-Costin, Luna, et al. ["Continuing WebAssembly with Effect Handlers."](https://dl.acm.org/doi/pdf/10.1145/3622814), OOPSLA, 2023.
- Watt, Conrad, et al. ["WasmRef-Isabelle: A Verified Monadic Interpreter and Industrial Fuzzing Oracle for WebAssembly."](https://dl.acm.org/doi/pdf/10.1145/3591224), PLDI, 2023.
- Romano, Alan, and Weihang Wang. ["When Function Inlining Meets WebAssembly: Counterintuitive Impacts on Runtime Performance."](https://dl.acm.org/doi/pdf/10.1145/3611643.3616311), FSE, 2023.
- Liu, Zhibo, et al. ["Exploring missed optimizations in webassembly optimizers."](https://www.cse.cuhk.edu.hk/~wei/papers/issta23_wasm.pdf), ISSTA, 2023.
- Titzer, Ben L. ["A fast in-place interpreter for WebAssembly."](https://dl.acm.org/doi/pdf/10.1145/3563311), OOPSLA, 2022.
- Jangda, Abhinav, et al. ["Not so fast: Analyzing the performance of WebAssembly vs. native code."](https://www.usenix.org/system/files/atc19-jangda.pdf), USENIX ATC, 2019.

## Applications in Security
*There are a lot of papers in this direction that are not listed in this repo.
- Wang, Yuanpeng, et al. ["Symgx: Detecting cross-boundary pointer vulnerabilities of sgx applications via static symbolic execution."](https://vtechworks.lib.vt.edu/bitstreams/4fb7d5ad-254d-4b31-9a52-640bd5c5956a/download), CCS, 2023
- He, Ningyu, et al. ["Eunomia: enabling user-specified fine-grained search in symbolically executing WebAssembly binaries."](https://arxiv.org/pdf/2304.07204), ISSTA, 2023.
- Romano, Alan, et al. ["Wobfuscator: Obfuscating javascript malware via opportunistic translation to webassembly."](https://par.nsf.gov/servlets/purl/10391578), S&P, 2022.
