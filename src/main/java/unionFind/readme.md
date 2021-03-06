# Union find (Disjoint-set)
wiki: https://en.wikipedia.org/wiki/Disjoint-set_data_structure

## 1. Basic union find
<div>
    <p>
        1. 
        <a href="https://www.lintcode.com/problem/connecting-graph/description">LintCode 589</a>:  
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/main/java/unionFind/LintCode589.java">Answer</a>, 
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/test/java/unionFind/LintCode589Test.java">Test</a>
    </p>
    <p><b>Description: </b>Basic union find with <i>Road compress</i> method used to reduce the 
    time complexity of <code>find()</code>. It's <code>O(1)</code> on average.</p>
</div>
<div>
    <p>
        2. 
        <a href="https://www.lintcode.com/problem/connecting-graph-ii/description">LintCode 590</a>:  
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/main/java/unionFind/LintCode590.java">Answer</a>, 
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/test/java/unionFind/LintCode590Test.java">Test</a>
    </p>
    <p><b>Description: </b>Follow up of <a href="https://www.lintcode.com/problem/connecting-graph/description">LintCode 589</a>. Besides get if 2 given nodes are connected. Return how many nodes the given node is connected with.
    Need an extra array with the same size of union find array to hold the count. Basically, always save and update the total count on the root node.</p>
</div>
<div>
    <p>
        3. 
        <a href="https://www.lintcode.com/problem/connecting-graph-iii/description">LintCode 591</a>:  
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/main/java/unionFind/LintCode591.java">Answer</a>, 
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/test/java/unionFind/LintCode591Test.java">Test</a>
    </p>
    <p><b>Description: </b>Follow up of <a href="https://www.lintcode.com/problem/connecting-graph/description">LintCode 589</a>. Calculate the total unique graph count. 
    Use a global count as initialized to the total number of nodes on start. When there is a connect & re-root operation, <code>count--</code>.</p>
</div>
<div>
    <p>
        4. 
        <a href="https://www.lintcode.com/problem/graph-valid-tree/description">LintCode 178</a>:  
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/main/java/unionFind/LintCode178.java">Answer</a>, 
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/test/java/unionFind/LintCode178Test.java">Test</a>
    </p>
    <p><b>Description: </b>Use union find to decide if the given 2-D array holds a valid tree. There should have and only have exactly one common father after 
    the uninon find "connect" operation for each edges. Otherwise, there can have more than one tree from the input.</p>
</div>

## 2. Union find in Map format
<div>
    <p>
        1. 
        <a href="https://www.lintcode.com/problem/find-the-weak-connected-component-in-the-directed-graph/description">LintCode 432</a>:  
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/main/java/unionFind/LintCode432.java">Answer</a>, 
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/test/java/unionFind/LintCode432Test.java">Test</a>
    </p>
    <p><b>Description: </b>Since the problem didn't assume the maximum number of verticies. We can't use a simple array in this problem 
    but rather to use the more complex form - <code>Map</code>. The key point is to write <i>Road compress</i> in Map form. And initialize the Map can be another point to think about.
     Basically we have to go through the entire graph once to record the vertices' label.</p>
</div>
<div>
    <p>
        2. 
        <a href="https://www.lintcode.com/problem/maximum-association-set/description">LintCode 805</a>:  
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/main/java/unionFind/LintCode805.java">Answer</a>, 
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/test/java/unionFind/LintCode805Test.java">Test</a>
    </p>
    <p><b>Description: </b>Use the <code>Map<String, String></code> to act as the union find array. After connect each other, find all the set and save their elements as separate list. 
    Then, iterate through the lists, return the largest one.</p>
</div>

## 3. 2-D union find
<div>
    <p>
        1. 
        <a href="https://www.lintcode.com/problem/set-union/description">LintCode 1396</a>:  
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/main/java/unionFind/LintCode1396.java">Answer</a>, 
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/test/java/unionFind/LintCode1396Test.java">Test</a>
    </p>
    <p><b>Description: </b>2-D union find. Treat each row as an element in union find. The final purpose is to count how many unique sets exist.
    Initialize a huge array to map values from set to a row. The default value is <code>-1</code> which represents mapping not exists yet.</p>
</div>

## 4. Number of Island Problem
<div>
    <p>
        1. 
        <a href="https://www.lintcode.com/problem/number-of-islands/description">LintCode 433</a>:  
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/main/java/unionFind/LintCode433.java">Answer</a>, 
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/test/java/unionFind/LintCode433Test.java">Test</a>
    </p>
    <p><b>Description: </b>There are many ways to solve the problem. However, in order to do the follow up question: # of Island II, I choose <b>union find</b> method to solve the problem.<br>
    The main point is that, construct the mapping between 2-D input array and 1-D union find array. Simply use <code>x * colLength + y</code> to get 1-D mapping.<br>
    Also, the union find array can be used as the set to prevent <b><a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/tree/master/src/main/java/bfs">BFS</a></b> traversing the same element more than once. Initially the value is <code>-1</code>(unvisited), if the input data in the specified gird if <code>true</code>, then change <code>father[x]=x</code>, else change the <code>father[x]=-2</code>.<br>
    If there are two <code>true</code> nearby, execute the <code>connect</code> operation to merge the union find.</p>
</div>
<b>Follow up question</b>:<br>
<div>
    <p>
        1. 
        <a href="https://www.lintcode.com/problem/number-of-islands-ii/description">LintCode 434</a>:  
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/main/java/unionFind/LintCode434.java">Answer</a>, 
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/test/java/unionFind/LintCode434Test.java">Test</a>
    </p>
    <p><b>Description: </b>Since we are using union find, there is no need to create the actual island array. Again, the union find array can be used as the set to avoid looking up same island more than once.<br>
    Unlike using <b><a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/tree/master/src/main/java/bfs">BFS</a></b> to traverse entire island map from previous problem, this problem can be solved by just iterating the input operators and take a look with the direction: up, down, left and right.</p>
</div>