# 📝 MY_WORK: Student Information, Development Log, Reflection & Answers

> This is the **only file** your instructor reads to grade Parts 3 and 4 (documentation and video). Everything you write here must be **in your own words**.

---

## 🛑 STOP: Read This Before You Do Anything Else

> ### 1️⃣ Read the whole `README.md` first
> The `README.md` in this repository contains the full instructions: how this assignment continues Assignment 1, the Chapter 5 recap, class descriptions, feature specifications, question prompts and the video script. **If you skip it, you will lose marks.**
>
> ### 2️⃣ Understand the full code before answering any question
> Open `SchedulerSimulationSync.java` and read it **from top to bottom**. You must be able to explain what `SharedStats`, `ReadyQueue`, `CpuWorker`, `RaceWindow.pause()`, `ReentrantLock` and `Semaphore` do **before** you write a single answer in Parts B and C. **Run the original starter first** (it is intentionally broken) and **save its output**: you need it for Question 1 of Part C.
>
> ### 3️⃣ Use only the code of this repository
> Work **only** on `SchedulerSimulationSync.java` from this repository. Do **not** copy or paste code from your previous assignments.
>
> ### 4️⃣ Commit many times, not once
> A single commit, or all commits made in the last hour, costs you **-0.5 mark**. See the [Commit Rules](#-commit-rules-mandatory) below.

**How to use this file:**
1. Fill in your **Student Information** (below) right now.
2. Follow the steps in the **Work Roadmap** in order.
3. Update the **Development Log** *every time* you work on the assignment, not at the end.
4. Do not delete any section header. Replace the `[...]` placeholders with your own text.

---

## 👤 Student Information

> ⚠️ **WARNING:** Fill this in first. Your name and ID must match the student ID you set in `SchedulerSimulationSync.java` (line 304) and the one you say in your video.

| Field | Your Answer |
|-------|-------------|
| **Full Name** | [haya ayed albagami] |
| **Student ID** | [446051371] |
| **University Email** | 446051371@std.psau.edu.sa |
| **GitHub Username** | [ioykr] |
| **Repository Link** | [https://github.com/ioykr/OS-Assignment3-haya-albagami] |
 
---

## 🎥 Video Link

**Video Link**: [Paste your video link here]

> ⚠️ **WARNING:** The video must be **publicly accessible** ("Anyone with the link can view") on **Google Drive**, **YouTube (Unlisted or Public)** or any other cloud file-sharing system. A private, restricted or broken link counts as a **missing video (-1 mark)**.
>
> 💡 **TIP:** Open the link in a **private/incognito window** before you submit. If it asks you to log in or request access, it is not public.
>
> 📌 **NOTE:** The link goes in **this file only** (`MY_WORK.md`), **not** in `README.md`. Name your video file `StudentID_Assignment3_Demo.mp4`. It must last **2 to 3 minutes**.

---

## 🗺️ Work Roadmap (follow in this order)

| Step | What to do | Where | Marks |
|:----:|------------|-------|:-----:|
| 0 | Read `README.md`, read the full code, **run the original starter and save its output** (it fails on purpose) | Your IDE | – |
| 1 | Fork, rename, keep the repo **PUBLIC**, set your student ID (line 304), **commit** | GitHub + code | Part 1 (1) |
| 2 | Feature 1: Mutex lock on the ready queue, **commit** | Code | Part 2 (0.25) |
| 3 | Feature 2: Mutex lock(s) on the shared statistics, **commit** | Code | Part 2 (0.25) |
| 4 | Feature 3: Counting semaphore instead of busy waiting, **commit** | Code | Part 2 (0.5) |
| 5 | Development Log (5+ entries, different dates) | This file, Part A | Part 3 (0.5) |
| 6 | Reflection (4 questions) | This file, Part B | Part 3 (0.5) |
| 7 | Technical Answers (4 questions) | This file, Part C | Part 3 (0.5) |
| 8 | Record the video, upload it, paste the link above | Video + this file | Part 4 (1.5) |
| 9 | Final check, then submit the repo link on Blackboard | Blackboard | – |

> 💡 **TIP:** Tick each step off as you go. Do not leave the log, the reflection or the video for the last day.

---

## 🔁 Commit Rules (MANDATORY)

> ### ⚠️ MANY COMMITS ARE REQUIRED. A single bulk commit is penalized (-0.5 mark).

**Minimum: 4 meaningful commits. Aim for 7 or more.**

| # | Commit | Example message |
|:-:|--------|-----------------|
| 1 | Student ID set | `Set my student ID: 441234567` |
| 2 | Feature 1: Ready queue lock | `Feature 1: Protected the ready queue with a ReentrantLock` |
| 3 | Feature 2: Statistics locks | `Feature 2: Added locks to the shared statistics counters` |
| 4 | Feature 3: Semaphore | `Feature 3: Replaced busy waiting with a counting semaphore` |
| 5 | Development log entries | `Docs: Added development log entries 1-3` |
| 6 | Reflection and answers | `Docs: Completed reflection and technical answers` |
| 7 | Video link | `Docs: Added demo video link` |

**Rules:**
- ✅ **One commit per feature.** Do not put all three features in one commit.
- ✅ **Commit after each work session**, and after each part of this file.
- ✅ **Spread your commits over different dates.** Not all in one day.
- ❌ **Do not make all commits in the last hour** before the deadline (November 14, 2026).
- ❌ **No vague messages** like `done`, `update` or `final version`.

> 💡 **TIP:** Your commit history is checked and you **show it in your video** (at least 4 commits visible). Your development log dates should match your commit dates.
>
> 💡 **TIP:** **Use VS Code** (see *Recommended Development Environment* in `README.md` for the full setup). Sign in to GitHub in VS Code, then commit from the Source Control panel (Ctrl+Shift+G) → stage → write a message → Commit → Sync/Push. You can edit and commit this file the same way. **Pushing** matters: commits that are not pushed to GitHub are invisible to the instructor.

---

# Part A: Development Log (0.5 mark)

> ⚠️ **WARNING:** Minimum **5 entries**, spread over **different dates**. Five entries written on the same day, or written all at once at the end, will lose marks and look like a copy. Entry dates should be **between the start of the assignment and the deadline (November 14, 2026)**.
>
> 💡 **TIP:** Write an entry at the **end of each work session**, while you still remember what happened. It takes 5 minutes.
>
> 💡 **TIP:** Be specific. "Worked on the code" is a weak entry. "Added a `ReentrantLock queueLock` to `ReadyQueue` and wrapped the body of `poll()` in `lock()` / `try` / `finally { unlock() }`" is a strong one.
>
> 📌 **NOTE:** Each entry needs: date and time, what you did, details, challenges, solution, and time spent. Real challenges are fine (and expected). Do not invent fake ones.

## Example Entry (do not copy it, write your own)

### Entry 1 - [November 2, 2026, 4:30 PM]
**What I did**: Forked the repository, set my student ID, and ran the original starter

**Details**:
- Forked the starter repository and renamed it
- Changed student ID on line 304 to my actual ID (441234567)
- Ran the original program: 4 CPUs started, three of them picked `P1`, then `IllegalThreadStateException` and the watchdog stopped the program
- Saved the output in a text file for Question 1
- Committed and pushed: `Set my student ID: 441234567`

**Challenges**: I did not understand why the same process was picked by three CPUs

**Solution**: Read `ReadyQueue.poll()` again and found the `RaceWindow.pause()` between reading the head and removing it

**Time spent**: 45 minutes

---

## Your Development Log

### Entry 1 - [11 november,7:00pm]
**What I did**:
Set up the GitHub repository and tested the original starter code
**Details**:
Connected my GitHub repository to VS Code.

Opened the project files and checked the assignment structure.

Set my student ID to 446051371.

Ran the original program and observed race condition errors, including NullPointerException and NoSuchElementException.
**Challenges**:
I had difficulty understanding why multiple CPUs were accessing the same process at the same time.
**Solution**:
I examined the ReadyQueue methods and identified the need for synchronization using ReentrantLock.
**Time spent**:
1 hour
---

### Entry 2 - [11 november,8:00pm]
**What I did**:
Implemented Feature 1– ReadyQueue synchronization.
**Details**:
Added a ReentrantLock named queueLock.

Protected add(), poll(), processOf(), and snapshot().

Used lock(), try, and finally to ensure the lock was always released.

Tested the changes and fixed code structure issues.
**Challenges**:
I encountered errors while running the program, especially in poll() and snapshot().
**Solution**:
 I corrected the critical sections and ensured that all accesses to the shared list and map were protected.
**Time spent**:
1 hour

---

### Entry 3 - [12 november,11:00am]
**What I did**:
Implemented Feature 2 – Shared Statistics synchronization
**Details**:
Added one ReentrantLock named statsLock.

Protected the three update methods and three getter methods.

Used try/finally in every protected method.

Tested the program and verified the context switches, completed processes, and total service time.
**Challenges**:
 I needed to understand how concurrent updates could cause lost updates in shared counters.
**Solution**:
I used one lock to protect all three shared statistics and their read and update operations.
**Time spent**:
1 hour

---

### Entry 4 - [12 november,12:00pm]
**What I did**:
Implemented Feature 3 – Counting Semaphore
**Details**:
Imported Java Semaphore.

Created a counting semaphore with an initial value of zero.

Added release() when a process is added to the ready queue.

Used acquire() in CpuWorker to block CPUs until a process becomes available.

Removed the busy-waiting polling mechanism.

Added shutdown signaling to wake up blocked CPUs when all processes were completed.
**Challenges**:
The most challenging part was understanding how to wake up CPUs without leaving any thread blocked forever
**Solution**:
I implemented the shutdown signal using release(totalCPUs).
**Time spent**:
1 hour

---

### Entry 5 - [12 november,1:00pm]
**What I did**:
Tested the final implementation and completed the feature commits.
**Details**:
Ran the program five consecutive times.

Verified that all four verification checks passed.

Confirmed that all 19 processes completed successfully.

Confirmed that busy-waiting polls were zero.

Committed and pushed the final Feature 3 implementation to GitHub
**Challenges**:
I needed to ensure that the program terminated correctly without exceptions or watchdog errors.
**Solution**:
I repeated the tests and checked the verification output after each run.
**Time spent**:
30 minutes
---

### Entry 6 - [Optional - Date and Time]
**What I did**:

**Details**:

**Challenges**:

**Solution**:

**Time spent**:

---

## Development Log Summary

> 💡 **TIP:** Fill this in **last**, after all entries are written.

**Total time spent on assignment**: [4.5 hours]

**Most challenging part**:
implementing Feature 3 using a counting semaphore. I needed to understand how CPUs could wait without busy waiting and how to wake them up when all processes were completed.
**Most interesting learning**:
I learned how ReentrantLock prevents race conditions and how Semaphore allows threads to wait efficiently without wasting CPU resources.
**What I would do differently next time**:
 I would study the synchronization concepts before starting the implementation. I would also test each feature immediately after completing it and review my code carefully before moving to the next feature.
---

# Part B: Reflection (0.5 mark)

> 🛑 **STOP:** Do **not** start this part until you have read the `README.md`, read the **entire** `SchedulerSimulationSync.java`, run it, and finished the three features.
>
> ⚠️ **WARNING:** Each answer must be **5 to 7 sentences**, in **your own words**. Copied or AI-generated answers without understanding get **0 marks for the whole assignment**. You may be asked to explain them in person.
>
> 💡 **TIP:** Mention concrete things you actually did: a method you wrote, an error you hit, a line of output you saw. Generic answers score low.
>
> 💡 **TIP:** Draft your answer in a few bullet points first, then turn them into sentences.

## Question 1: What did you learn about synchronization?

> 💡 **TIP:** Talk about race conditions (read-modify-write), critical sections, mutual exclusion with `ReentrantLock` and `try/finally`, the role of a counting semaphore, and what surprised you when the starter failed.

**Your Answer:** *(5-7 sentences)*

[I learned that synchronization is important when multiple threads access the same shared data. A race condition can happen when two threads read and update a value at nearly the same time, causing a lost update. A critical section is the part of the code that accesses shared data, and mutual exclusion allows only one thread at a time to enter it. In this assignment, I used ReentrantLock to protect the ReadyQueue and SharedStats data. I used try/finally so unlock() is called even if the method returns early or an exception occurs. I also learned that a counting Semaphore allows a CPU to wait using acquire() until a process becomes available instead of repeatedly checking the queue. The original starter surprised me because it produced NoSuchElementException in poll() and NullPointerException in snapshot().]

## Question 2: What was the most challenging part of this assignment?

> 💡 **TIP:** Pick **one** specific challenge (understanding why the starter failed, choosing the lock granularity, the initial value of the semaphore, the shutdown of the CPUs, Git, the video) and say *why* it was hard.

**Your Answer:** *(5-7 sentences)*

[The most challenging part was understanding how to use the counting Semaphore to stop busy waiting and shut down the CPUs. At first, I understood that add() should call release() and a CPU should call acquire() before taking a process. The difficult part was understanding what happens after the last process finishes. CPUs that are blocked in acquire() will not automatically wake up just because all processes are completed. I learned that release(totalCPUs) provides permits to wake up the waiting CPUs. After waking up, each CPU must check the completed process count and exit instead of trying to take another process.]

## Question 3: How did you overcome the challenges you faced?

> 💡 **TIP:** Describe your method: reading the slides and the documentation, adding `System.out.println` to debug, running the program many times, re-reading the README, testing after each small change, asking for help.

**Your Answer:** *(5-7 sentences)*

[I overcame the challenges by following the assignment in small steps and checking one part at a time. I first ran the original starter with my student ID and saved the output. That run showed NullPointerException in ReadyQueue.snapshot() and NoSuchElementException in ReadyQueue.poll(), and the verification values were incorrect. I reviewed the affected methods and identified that the shared list and map needed mutual exclusion. I then protected the ReadyQueue methods with queueLock and used try/finally to release the lock safely. I also reviewed the statistics lock and semaphore logic against the README requirements before moving to the next feature.]

## Question 4: Where can synchronization concepts be applied in real-world applications?

> 💡 **TIP:** Use real applications you know (banking and money transfers, ticket or seat booking, a shared counter on a website, a print queue, a database) and connect each one to what you built here (shared data, critical section, lock or semaphore).

**Your Answer:** *(5-7 sentences)*

[Synchronization is important in applications where several users or threads access the same data. In a banking system, a lock can protect an account balance so two withdrawals do not overwrite each other's updates. In ticket booking systems, synchronization can prevent two customers from reserving the same seat. Databases use locks to coordinate transactions that read or update shared records. A print queue can use a semaphore to notify a printer worker when a new job is available. These examples are similar to my scheduler because queueLock protects shared queue data and the semaphore controls when CPUs can continue working.]

### Optional: What would you like to learn more about?

[Any topics related to synchronization or operating systems that you're curious about?]

### Optional: How confident do you feel about synchronization concepts now?

[Beginner / Intermediate / Confident. What do you understand well? What needs more practice?]

### Optional: Feedback on the assignment

[Any comments? Was it helpful? Too easy or hard? Suggestions?]

---

# Part C: Technical Answers (0.5 mark)

> 🛑 **STOP:** You cannot answer these questions without understanding the code. Re-read `SchedulerSimulationSync.java` and **run it** first. Your answers must reference **your own code and your own output** (your student ID makes your output and your expected values unique).
>
> ⚠️ **WARNING:** Each answer must be **3 to 5 sentences**, with specific examples from your code or output. Use correct terms: race condition, critical section, mutual exclusion, mutex lock, semaphore, busy waiting, deadlock, producer, consumer.
>
> 💡 **TIP:** Keep the output of the **original starter** and the output of your **final version** in text files or screenshots, so you can copy real snippets for Question 1.

## Question 1: Race Condition in Your Own Output

**Question**: Run the **original starter** (before any fix) and paste the **verification block** of that run. Which value was wrong (expected vs observed)? Explain **step by step**, with two named threads/CPUs, how **one lost update** happens on one of the shared variables (read, `RaceWindow.pause()`, write). Why can the same bug happen on a real machine even without `RaceWindow`, and why is it hard to detect?

> ⚠️ **WARNING:** The snippet must come from **your own run** (with your student ID), not from a classmate or from this README.
>
> 💡 **TIP:** Use a small timeline: *CPU-1 reads `contextSwitchCount` = 12 → CPU-2 reads 12 → CPU-1 writes 13 → CPU-2 writes 13 → one increment is lost.* If your starter run crashed before printing numbers, run it several times (or paste the exception and the watchdog message and explain it).

**Your Answer:** *(3-5 sentences)*

[My original starter run did not complete a normal lost-update demonstration because the CPU threads failed first while accessing ReadyQueue. CPU-2, CPU-3, and CPU-4 threw NullPointerException in snapshot(), while CPU-1 threw NoSuchElementException in poll(); the verification showed expected values of 40, 19, and 159075 but observed 0 for all three. A possible lost update in SharedStats can happen when CPU-1 reads contextSwitchCount = 12, CPU-2 also reads 12, and both pause at RaceWindow.pause() before writing 13, although the correct result should be 14. The same problem can happen on a real machine without RaceWindow because the operating system may switch between threads after a read and before the corresponding write. It is difficult to detect because thread execution timing changes between runs, so the error may appear in some runs but not others.]

Verification block of the **original starter**:
═══ VERIFICATION (expected values are computed from YOUR seed) ═══
Context switches (quanta executed) expected 40 observed 0 ✘ MISMATCH
Completed processes expected 19 observed 0 ✘ MISMATCH
Total service time (ms) expected 159075 observed 0 ✘ MISMATCH
Busy-waiting polls (must be 0) expected 0 observed 0 ✔
✘ At least one check failed (see the ✘ lines above): a race condition or busy waiting is still present.

Verification block of **my final version**:
```
═══ VERIFICATION (expected values are computed from YOUR seed) ═══
Context switches (quanta executed)     expected 40       observed 40       ✔
Completed processes                    expected 19       observed 19       ✔
Total service time (ms)                expected 159075   observed 159075   ✔
Busy-waiting polls (must be 0)         expected 0        observed 0        ✔
✔ All shared values are consistent.
```

**Explanation of the timeline:**
[CPU-1 reads contextSwitchCount = 12. CPU-2 also reads 12 before either thread writes the updated value. Both threads execute RaceWindow.pause(), creating time for the interleaving. CPU-1 writes 13, and CPU-2 then also writes 13. The correct value should be 14, so one increment is lost.]

## Question 2: Critical Sections and Lock Granularity

**Question**: List the **critical sections** you protected (variables and methods) and the lock(s) you used. **Lock granularity:** did you use **one lock** for the three statistics or **one lock per variable**? Why, and what is the trade-off? Why is the **ready queue** protected by a **different** lock than the statistics? Explain how your solution provides **mutual exclusion**, and discuss **progress** and **bounded waiting** (a default `ReentrantLock` is not fair: what does that imply?).

> 💡 **TIP:** The three counters are independent: does updating `contextSwitchCount` need to block an update of `totalServiceTime`? Also think about what could go wrong (deadlock, or long waiting) if the queue lock and the statistics lock were the **same** lock and a thread held it while doing something slow.

**Your Answer:** *(3-5 sentences)*

[I protected the ReadyQueue list and map in add(), poll(), processOf(), and snapshot() using queueLock. I protected the three SharedStats variables in all three update methods and all three getter methods using one statsLock. I chose one lock for the statistics because it is simpler to manage, but the trade-off is that operations on independent counters must wait for each other. I used a separate queueLock because the queue and statistics are different shared resources, reducing unnecessary blocking between unrelated operations. Each lock provides mutual exclusion, and after a thread releases the lock in finally, another waiting thread can proceed; however, the default non-fair ReentrantLock does not guarantee FIFO order or bounded waiting, so starvation is possible.]

| Critical section (variable / method) | Lock used | Why it needs protection |
ReadyQueue.add()	|queueLock	|Protects the queue when adding processes.
ReadyQueue.poll()	|queueLock	|Prevents two CPUs from taking the same process.
ReadyQueue.processOf()	|queueLock	|Protects access to the shared process map.
ReadyQueue.snapshot()	|queueLock	|Prevents concurrent modification during iteration.
incrementContextSwitch()	|statsLock	|Prevents lost updates to the context switch counter.
incrementCompletedProcess()	|statsLock	|Prevents lost updates to the completed process counter.
addServiceTime()	|statsLock	|Protects the total service time during updates.
getCompletedProcessCount()	|statsLock	|Protects reading the completed process counter.
getContextSwitchCount()	|statsLock	|Protects reading the context switch counter.
getTotalServiceTime()	|statsLock	|Protects reading the total service time.

## Question 3: Busy Waiting vs Semaphore

**Question**: Describe the **busy waiting** of the starter and its cost (give the `Busy-waiting polls` number from your **starter** run). What does the **value of your semaphore** represent? What is its **initial value** and why? What is its value right after the `numProcesses` initial `add()` calls? Why does the last CPU call `release(totalCPUs)` at the end, and what would happen if it did not?

> 💡 **TIP:** Think about what a CPU does when the queue is empty in the starter, and what a CPU does in your final version (is it running, ready or blocked?). Also check what happens to a CPU blocked in `acquire()` when no process will ever be added again.

**Your Answer:** *(3-5 sentences)*

[In the original starter, CPUs used busy waiting by repeatedly checking the ready queue and sleeping for 20 milliseconds when it was empty, which wastes CPU time. My original run showed 0 busy-waiting polls, but this does not mean busy waiting was solved because the CPU threads crashed before reaching the polling stage. The semaphore starts at 0 because no processes are available initially, and after the 19 initial add() calls its value becomes 19 because each call releases one permit. Each CPU uses acquire() to consume a permit when a process is available and blocks when no permit exists. When all processes finish, release(totalCPUs) wakes up the blocked CPUs so they can check the completion count and exit; otherwise, they may remain blocked forever.]

## Question 4: Classical Problems and Deadlock

**Question**: The CPUs and the ready queue look like a classical synchronization problem of Chapter 5. **Name it**, and say who plays the **producer** and the **consumer** roles (careful: here the CPUs also re-enqueue processes). If the ready queue were **bounded** (capacity `K`), name the **three semaphores** you would need and their **initial values**. Describe a **deadlock scenario** that appears if a thread acquired the **mutex before** waiting on the semaphore (or if two locks were acquired in different orders), and say **which of the four necessary conditions** you would break to prevent it.

> 💡 **TIP:** Recall the bounded-buffer solution of the slides (`empty`, `full`, `mutex`) and the order of `wait()` calls in the producer and the consumer. For the deadlock, think about a producer that holds the mutex while waiting for a free slot that only a consumer (who needs the mutex) can create.

**Your Answer:** *(3-5 sentences)*
This assignment is an example of the Producer-Consumer problem. The main thread is the initial producer, while the CPUs are consumers that take processes from the ready queue and also become producers when they re-add unfinished processes. If the ready queue has a capacity of K, we need three semaphores: empty = K, full = 0, and mutex = 1. Deadlock can happen if a producer holds the mutex while waiting for an empty slot because the consumer needs the same mutex to remove a process and create an empty slot. We can prevent this by waiting for the empty semaphore before acquiring the mutex, which breaks the hold-and-wait condition.
**Classical problem and roles**:
[Producer-Consumer problem.
The main thread is the initial producer, and CPUs are consumers. CPUs also become producers when they re-add unfinished processes to the ready queue.]

**Semaphores for a bounded queue (name and initial value)**:
[empty = K, full = 0, mutex = 1]

**Deadlock scenario and prevention**:
[A producer may acquire the mutex before waiting for an empty slot. If the queue is full, the consumer cannot acquire the mutex to remove a process and free a slot. We prevent this by waiting for the empty semaphore before acquiring the mutex, which breaks the hold-and-wait condition].

## Summary

**Key concepts I understood through these questions:**
1.Race conditions and how ReentrantLock protects shared data.

2.How Semaphore prevents busy waiting.

3.The Producer-Consumer problem and mutual exclusion.

**Concepts I need to study more:**
1.Deadlock and its four necessary conditions.
2.Semaphore operations and bounded waiting.

---

# ✅ Final Checklist (complete before submitting)

> ⚠️ **WARNING:** Go through every line. Blackboard does not accept submissions after the deadline, which is **November 14, 2026**.

**Repository**
- [ ] Repository is **PUBLIC** (Settings → Danger Zone → Visibility)
- [ ] Repository is renamed to `OS-Assignment3-YourFirstName-YourLastName`
- [ ] GitHub account uses the university email (`@std.psau.edu.sa`)

**Code**
- [ ] Student ID is set in `SchedulerSimulationSync.java` (line 304)
- [ ] My code is based **only** on the starter of this repository (nothing copied from previous assignments)
- [ ] Code compiles and runs with no errors, and terminates by itself (no `⛔ WATCHDOG`)
- [ ] Feature 1 (ready queue lock), Feature 2 (statistics locks) and Feature 3 (semaphore, no busy waiting) all work
- [ ] **The four verification lines are ✔ in 5 consecutive runs**
- [ ] Every lock is released in a `finally` block
- [ ] `RaceWindow`, `Config`, the verification block and the watchdog are **unchanged**
- [ ] Each feature has clear comments

**Commits**
- [ ] **At least 4 meaningful commits, ideally 7 or more**
- [ ] **One commit per feature**
- [ ] Commits are spread over **different dates** (not all in the last hour)
- [ ] Everything is **pushed** to GitHub

**This file (`MY_WORK.md`)**
- [ ] Full name and student ID filled in at the top
- [ ] Development log has **5+ entries** on different dates
- [ ] Reflection: 4 questions, 5-7 sentences each
- [ ] Technical answers: 4 questions, 3-5 sentences each, with examples from **your** output (starter output **and** final output pasted in Question 1)
- [ ] No `[...]` placeholders left
- [ ] No section headers deleted

**Video**
- [ ] 2-3 minutes long, named `StudentID_Assignment3_Demo.mp4`
- [ ] Shows your name, ID, repository, 3 features (and your lock granularity choice), IDE execution with the verification block, one synchronization concept, and commit history
- [ ] Link is **public** (tested in an incognito window) and pasted in the **Video Link** section above

**Blackboard**
- [ ] Submit **only** the link to your public GitHub repository

> 🎯 **Good luck!** Start early, commit regularly, and make sure you can explain every line you submit.
