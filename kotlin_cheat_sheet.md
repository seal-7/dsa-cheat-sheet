# 🧠 Kotlin Coding Interview Cheat Sheet (DSA + Patterns)

This file is designed to **stop you from looking up syntax** during interviews.
Memorize **patterns**, not APIs.

---

## 1️⃣ Frequency Map (Very Common)

```kotlin
val freq = HashMap<Int, Int>()
for (x in nums) {
    freq[x] = freq.getOrDefault(x, 0) + 1
}
```

---

## 2️⃣ Top K Elements (Max Heap)

```kotlin
val pq = PriorityQueue<Pair<Int, Int>>(
    compareByDescending { it.second }
)

for ((num, count) in freq) {
    pq.offer(num to count)
}

val res = IntArray(k)
for (i in 0 until k) {
    res[i] = pq.poll().first
}
```

---

## 3️⃣ Sorting

```kotlin
nums.sort()

val arr = s.toCharArray()
arr.sort()
val sorted = String(arr)
```

---

## 4️⃣ Two Pointers

```kotlin
var l = 0
var r = arr.lastIndex

while (l < r) {
    l++
    r--
}
```

---

## 5️⃣ Sliding Window

```kotlin
var left = 0
for (right in nums.indices) {
    while (/* invalid */) {
        left++
    }
}
```

---

## 6️⃣ Stack (ArrayDeque)

```kotlin
val stack = ArrayDeque<Int>()
stack.addLast(x)
stack.removeLast()
stack.last()
```

---

## 7️⃣ Tree DFS

```kotlin
fun dfs(node: TreeNode?): Int {
    if (node == null) return 0
    return maxOf(dfs(node.left), dfs(node.right)) + 1
}
```

---

## 8️⃣ BFS

```kotlin
val q = ArrayDeque<Int>()
q.addLast(start)
while (q.isNotEmpty()) {
    q.removeFirst()
}
```

---

## 9️⃣ Bit Manipulation

```kotlin
a and b
a or b
a xor b
a shl k
a shr k
a ushr k
a.inv()
```

---

## 🔟 DP (1D)

```kotlin
val dp = IntArray(n + 1)
for (i in 2..n) {
    dp[i] = dp[i - 1] + dp[i - 2]
}
```

---

## 1️⃣1️⃣ DP (2D)

```kotlin
val dp = Array(r) { IntArray(c) }
```

---

## 1️⃣2️⃣ Priority Queue

```kotlin
val minHeap = PriorityQueue<Int>()
val maxHeap = PriorityQueue<Int>(compareByDescending { it })
```

---

## 1️⃣3️⃣ Printing

```kotlin
println(arr.contentToString())
```

---

## FINAL RULE

Memorize **patterns**, not syntax.
