## What is a Binomial Distribution?

A binomial distribution is a a discrete probability distribution that describes the number of successes where there are two possible outcomes, under the following assumptions:

1. **Fixed Number of Trials ($n$)**: Consisting of a fixed number of independent trials, denoted by $n$. Each trial can result in one of two outcomes: success or failure.
    
2. **Independent Trials**: Each trial is independent of the others. The outcome of one trial does not affect the outcome of any other trial.
    
3. **Constant Probability of Success ($p$)**: The probability of success, denoted by $p$, remains constant from trial to trial.

> [!info]- Denotation
> If X follows a binomial distribution:
> It can be denoted as $X \sim B(n,p)$
> > [!tip] $X \sim \dots$
> >
> > $X:$ represents a variable, likely representing the number of successes.
> > $\sim:$ (Tilda) "follows" or "is distributed as".
> 
> > [!tip] $B(n,p)$
> > $B :$ Indicates a binomial distribution
> > $n :$ number of trials
> > $p :$ probability of success
> 
> 
> So for example: $X \sim B(20,0.5)$
> 
> We are declaring $X$ has a binomial distribution with 20 trials each with a 50% chance of success

> [!abstract]- Visualisation 
> The distribution can be represented visually using a vertical line graph
> 
> > [!example] $p: 0.2$ 
> > ![[Pasted image 20240419140528.png]]
> > Graph has a tail to the right
>
> > [!example] $p: 0.8$ 
> >  ![[Pasted image 20240419140617.png]]
> > Graph has a tail to the left
>
> > [!example] $p: 0.5$ 
> > ![[Pasted image 20240419140555.png]]
> > Graph is symmetrical

> [!tip] Exam Tip
> If you are asked to criticise a binomial model always consider whether the trials are independent, this is usually the one that stops a variable from following a binomial distribution!


---

## Probability Questions

> [!example]- Simple Game
> A game consists of 10 points, each of which can be won or lost with 0.65 chance of winning. Find the probability of scoring at least 7 points
> 
> We can use binomial expansion to work out the probability 
> 
> Since we are finding the probability of scoring 7 or more points, we are going to do a right tailed test
> We select the right tailed option $(X\ge)$
> 
> $x:7$
> $n:10$
> $p: 0.65$
> 
> Which gives us $P(X\ge 7) = 0.5138$

> [!example]- Recursive Simple Game
> A game consists of 10 points, each of which can be won or lost with 0.6 chance of winning. Find the probability of scoring at least 7 points
> 
> using calc: $P(X \ge 7)= 0.3822$
> 
> The game above is played 3 times, find the probability of scoring at least 7 points in exactly two of the three games
> 
> $P(P(X \ge 7) = 2)$
> $P(P(0.3822) = 2) = 0.2707$
> $\t{where}\;n = 3,\; p = 0.3822$

> [!example]- Sweet manufacturer
> 
> > A manufacturer of sweets knows that 8% of the bags of sugar delivered from supplier A will
> > be damp.
> > 
> > A random sample of 35 bags of sugar is taken from supplier A.
> 
> > [!question]- **(a)** Using a suitable model, find the probability that the number of bags of sugar that are damp is:
> > 	
> > > [!info] $n = 2$
> > > 
> > > We can use the binomial distribution to find out this probability
> > > 
> > > $\t{Tail} : (X=)$
> > > $x : 2$
> > > $n : 35$
> > > $p : 0.08$
> > > 
> > > $P(X=2) = 0.243$
> > 	
> > > [!info] $n > 3$
> > > 
> > > $\t{Tail} : (X\ge)$
> > > $x : 4$
> > > $n : 35$
> > > $p : 0.08$
> > > 
> > > $P(X\ge4) = 0.306$
> 
> > Supplier B claims that when it supplies bags of sugar, the proportion of bags that are
> > damp is less than 8%
> > 
> > The manufacturer takes a random sample of 70 bags of sugar from supplier B and finds
> > that only 2 of the bags are damp.
> 
> > [!question]- **(b)** Carry out a suitable test to assess supplier B’s claim.
> > 
> > You should state your hypotheses clearly and use a 10% level of significance.
> > 
> > *Let $p$ be the probability of a bag of sugar being damp*
> > 
> > $H_0 : p = 0.08$
> > $H_1 : p < 0.08$
> > 
> > $X = 2$
> > $n : 70$
> > 
> > We are going to do a left tailed p-value test at a 10% level of significance
> > 
> > $X\sim B(70, 0.08)$
> > 
> > $\t{Tail} : X \le$
> > $X:2$
> > $n:70$
> > $p:0.08$
> > 
> > $P(X\le2) = 0.0739756\dotsb$
> > $P(X\le2) = 0.074$
> > 
> > $\cancel{\therefore \t{supplier B's claim is correct}}$
> > 
> > $X\le2 \;\t{is within the critical region}$
> > $\t{We reject}\; H_0$
> > $\therefore \t{there is evidence to support supplier B's claim}$
> > 
> 

> [!example]- Manon's spinners
> 
> > Manon has two biased spinners, one red one green.
> 
> > The random variable $R$ represents the score when the red spinner is spun.
> > The random variable $G$ represents the score when the green spinner is spun.
> 
> > The probability distributions for $R$ and $G$ are given below.
> 
> 
> | $r$      | $2$           | $3$           |
> | -------- | ------------- | ------------- |
> | $P(R=r)$ | $\frac{1}{4}$ | $\frac{3}{4}$ |
> | $g$      | $1$           | $4$           |
> | $P(G=g)$ | $\frac{2}{3}$ | $\frac{1}{3}$ |
> 
> 
> 
> > Manon spins each spinner once and adds the two scores.
> 
> > [!question]- **(a)** Find the probability that $\dots$
> > 	
> > > [!info] **(i)** the sum of the two scores $= 7$
> > > 
> > > The only way for the sum of spinner's scores to be 7 is such that $r = 3$ and $g = 4$
> > > 
> > > $P(r = 3) = \frac{3}{4}$
> > > $P(g = 4) = \frac{1}{3}$
> > > 
> > > $P(r = 3 \cap g = 4) = 1/4$
> > 
> > > [!info] **(ii)** the sum of the two scores is $< 4$
> > > 
> > > The only way for the sum of spinner's scores to be less than 4 is such that $r = 2$ and $g = 1$
> > > 
> > > $P(r = 2) = \frac{1}{4}$
> > > $P(g = 1) = \frac{2}{3}$
> > > 
> > > $P(r = 2 \cap g = 1) = \frac{1}{6}$
> > 
> 
> The random variable $X = mR + nG$ where $m$ and $n$ are integers.
> 
> $$P(X=20) = \frac{1}{6} \;\;\t{and}\;\; P(X=50)=\frac{1}{4}$$
> 
> > [!question]- **(b)** Find the value of $m$ and the value of $n$
> > 
> > $P(X=20) = \frac{1}{6}$
> > 
> > $\frac{1}{6} \div \frac{1}{4} = \frac{2}{3}$
> > 
> > $P(R = 2) = \frac{1}{4}$
> > $P(G = 1) = \frac{2}{3}$
> > 
> > $\r 20 = 2m + n$
> > 
> > ---
> > 
> > $P(X=50)=\frac{1}{4}$
> > 
> > $\;\cancel{\frac{1}{4} \div \frac{1}{4} = \frac{1}{16}}$
> > 
> > $\;\;\frac{1}{4} \div \frac{3}{4} = \frac{1}{3}$
> > 
> > $P(R = 3) = \frac{3}{4}$
> > $P(G = 4) = \frac{1}{3}$
> > 
> > $\r 50 = 3m + 4n$
> > 
> > ---
> > 
> > $20 = 2m + n$
> > $n = - 2m + 20$
> > 
> > $50 = 3m + 4(-2m + 20)$
> > $50 = 3m -8m + 80$
> > $30 = 5m$
> > 
> > $\underline{m = 6}$
> > 
> > $20 = 2\times6 + n$
> > $\underline{n = 8}$
> > 
> > $50 = 3\times6 + 4 \times 8$
> > $20 = 2\times 6 + 8$
> 