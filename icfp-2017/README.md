ICFP 2017

DISCLAIMER, These are rough notes of ICFP sessions that i attended and may not be accurate.
Please check the papers/videos to revalidate what all being said here.

This was the first time when ICFP was collocated with FSCD (Formal structure of
computation and deduction). Also, ICFP members are looking at co-locating with POPL.
That makes me very excited as it will provide a single platform for the programming
language research

## Sunday

I attended PLMW 2017, after being suggested by multiple people, hoping that it would
cover some basics on functional programming research topics and areas of research.

### Keynote By Chris -

Tags: Programming language Research, Ph.D, finding a research thesis, role of advisor

Chris is an assistant professor at North Carolina State. Unfortunately, I don't
remember much of the talk and I didn't take the notes :(. AFAIR, the talk was about
how she found her research topic. She was interested in automated reasoning, linear logic
in arts, games, narratives. She encouraged inter/anti-disciplinary research - ai, games, generative
narrative, automated reasoning in her case. And how working with people from different diversity helped.
She also said the key is finding an advisor who's modus of operandi align with you.
She also talked about her research which I don't remember much -- see Keynote1
for more info

### A few frank remarks - Conor McBridge

The key idea was applicability of research on computer languages. He gave an exmaple of
pattern matching which was invesnted by his dad in 1967 which was implemented in objectiveC in 2014.
Not sure why he choose objectiveC - maybe he treats objectiveC a launguage of masses?
Not scala?

### Compositional Compiler Correctness - Amal ahmed

Amal ahmed has been in language and verification research for more than 10 years. The talk was
clear and crisp. She talked about the challenges of whole program verification. We have
CompCert C verification compiler and Leroy's 06 research. We want the compiler to
verify "some"? (i don't remember what can be verified) properties at the time of
linking with shared objects.
So how do we verify linked code when complier won't have access to the code. She talks
how we can establish equivalence b/w the source and target. Some other challenges are
linked libraries can have the different source from the application source. What if linked
libraries source don't provide the same gurrantess/invariants?

### RustBelt By Derek?

Derek talked about the how Rust achieves object ownership guarantees at the compile time.
Rust defines types that provide the semantics of READ, WRITE, READ-SHARED, etc.. That
allows compiler to verify the invariants aren't violated. The talk was easy to follow.

### Handling fibered algebraic effects

Can't remember

### Only control effects and dependent types

Can't remember. I blame the assent.

I missed the evening session. Met up with some friends in London.

## Monday - start of ICFP

### Compositional creativity
TODO: saw it at home because i was deprived of sleep

### Getting my sleep back

### A unified approach to solving seven programming problems (functional pearl)
I came in at the end of the talk. Was disoriented because i thought the talks
would have the same schedule as Sunday but I was wrong. Meh. Can't remember

### Query generation using COQ
Meh

### A framework for adaptive diff privacy

Anonymization doesn't work at scale. Diff privacy - cost of each field, divided
into curator and analyst, it is compositional. Contribution - presentation of adaptive fuzz?
which has the novel semantics of adaptive diff privacy. The language has the dependent
types.

### Symbolic conditioning array in probabilistic programming
Meh

### Abstracting definational interpreters

* y-combinator? fixed point -- stopping point of recursion? Can't remember

### On the power experesive power of user defined effects
 Can't remember

### Imperative functional programs that explain their work
Cant remember

### Effect-driven quick checking of Compilers

## Tuesday

### [Keynote - Assuring AI](https://livestream.com/oxuni/ICFP-2017/videos/162312916)

In summary, John talked about the types of AI systems, how they are verified, what are the challenges and research topic.
He didn't have answers; He was asking the questions.
How good are the models? How much testing have we done? [Galios] defined intelligence
as Perceiving, learning, abstract, and reasoning. Turbox tax
is the 1st type of system - high on reasoning but low on other properties.
The 2nd level of AI systems
like deep learning models - high on all the properties but low on the reasoning. He briefly touched
how deep learning models work -- linear models with so many layers. He talked about
the challenges -- converging the models, how deep learning models can be
attached by adding a certain type
of noise which would make them fail all the time. But when interpreted by human,
they will guess them correctly.

### Kami: A platform for high level parametic hardware specification

### Spaceserch

### Compiling to categories

## Wednesday
No keynote on wednesday, only research presentations

### Herbarium Racketensis: A Stroll through the Woods
Some Racket dark magic which i don't remember

### A Specification for Dependent Types in Haskell
hmm, I don't recall Senator.

### Normalization by eval for sized-dependent types (TODO: recheck)

### Whip - high order contracts for modern services

Allows to define constraint in a high level language. It samples network traffic and
decodes the protocol (thrift and http+REST are supported?) and validates the contracts
constraints. Sends clear error message to the client/server (depending upon the topology
of whip deployment) that quickly help troubleshoot the problem

### Theorems for free for free: Parametricity, With and Without Types
It is correction and improvement on the work Amal did 5 years ago. It is proof
that parametricity is preserved when you cast a dynamic type to a static parametric
type in a gradually typed language.

### On Polymorphic Gradual Typing
No idea

### Gradual Typing with Union and Intersection Types
Add support for union and intersection types in gradual type system so that compiler
can do the verification. e.g.
```
# gradual typed function
let f (condition: bool) (x: ?): ?

# with union type
let f (condition: bool) (x: (int|bool)): (int |bool)
```
### Constrained Type Families
"Something" is wrong with Haskell type families and constrained type families is
the solution? Yes.

### Automating Sized-Type Inference for Complexity Analysis
Allow programmers to precisely define memory constraint on the app memory. The compiler can figure out
the object sizes as size is encoded in the type?
a powerful type system for size analysis. So you can define constraints on the
space complexity of your program and compiler can verify if your program holds
them or not.

## Thrus

### haskell at scala in Facebook
It is used for abused system which is a rule and machine learning based system.
It is run on thousand of machines. Latency and throughput sensitive.

* Type system makes it easy to root out bunch of problems
* automated testing like production which gives developers the feedback how the code
change affect latency and throughput before the merge??
* Small DSL which abstracts concurrency/parallelism
* Use applicatives for parallelism which makes sense. Monads depend upon the result
of previous operations.
* They make use of NUMA to keep memory local to the nodes
* They make optimization in haskell GC - i think they made smaller memory slabs

## Fri
TODO:

## Cool talks that I missed
* Recalling a witness
* Cogent: giving systems engineer a stepping stone
* Writing verified programs in CakeML
* Programming pearls on Monday

## References
* https://icfp17.sigplan.org/
* [Recorded sessions](https://livestream.com/oxuni/ICFP-2017)

