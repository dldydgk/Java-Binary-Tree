# Java-Binary-Tree
자바 자료구조 이진트리(Binary Tree)

## 1) 이진트리
모든 노드들의 자식 노드가 두 개 이하인 트리를 의미하는데, 다음은 이진 트리의 예다. 이런 이진 트리에서는 서브 트리가  두 개 이하기 때문에 서브 트리는 왼쪽 서브 트리와 오른쪽 서브 트리로 구분한다.

![image](https://github.com/dldydgk/Java-Binary-Tree/assets/126844590/49904653-97a8-4917-924e-0d43f9c72606)



#### 이진 트리 노드 생성 자바 코드▼
``` java
package sungil_2022_03;
public class Node {
	private int date;
	private Node left;
	private Node right;
	Node leftChild, rigthChild;
	
	public Node(int date, Node left, Node right) {
		this.date = date;
		this.left = left;
		this.right = right;
	}
	
	public int getDate() {
		return date;
	}
	public void setDate(int date) {
		this.date = date;
	}
	public Node getLeft() {
		return left;
	}
	public void setLeft(Node left) {
		this.left = left;
	}
	public Node getRight() {
		return right;
	}
	public void setRight(Node right) {
		this.right = right;
	}
}
```

## ● 완전 이진 트리(complete binary tree)
단말 노드를 제외한 나머지 노드가 두 개의 자식 노드를 가지고 있는 트리.
A, B, C, D 노드는 모두 두 개의 자식 노드를 가지고 있다

 ![image](https://github.com/dldydgk/Java-Binary-Tree/assets/126844590/6655d332-50a6-40ff-a07c-a2c69f171c79)



## 2) 이진 탐색 트리(Binary Search Tree)
 이진 탐색 트리(binary search tree)는 데이터의 삽입, 삭제, 탐색 등이 자주 발생하는<br>
 경우에 효율적인 구조로, 이진 트리이면서 같은 값을 갖는 노드가 없어야 한다.
 왼쪽 서브 트리에 있는 모든 데이터는 현재 노드의 값보다 작고,
 오른쪽 서브 트리에 있는 모든 노드의 데이터는 현재 노드의 값보다 크다.



## ● 데이터 탐색은 루트에서부터 시작된다.
- 루트 노드의 데이터와 찾으려는 데이터를 비교하여 같으면 탐색은 성공 종료
- 루트 노드가 작으면 루트 노드의 오른쪽
- 루트 노드가 크면 루트 노드의 왼쪽


## 3) 이진 트리 삽입
이진 탐색 트리에서의 삽입은 탐색 동작을 통해 이루어진다. 탐색에 성공하면 삽입은 실패하는데, 이는 이진 탐색 트리는 같은 데이터를 갖는 노드가 없어야 하기 때문이다.
반면에 탐색에 실패하면 삽입을 할 수 있으며, 탐색에 종료된 지점의 데이터를 값으로 하는 노드가 삽입된다.
삽입할 위치는 루트 노드에서부터 시작되며 삽입할 노드의 데이터가 비교하는 노드의 데이터보다 작으면 왼쪽 서브 트리로 진행하고 크면 오른쪽 서브 트리로 진행한다.

![image](https://github.com/dldydgk/Java-Binary-Tree/assets/126844590/5fa77684-568f-461b-9bb1-01f4a21d7944)



