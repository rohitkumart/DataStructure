class Node{
    constructor(val, next = null){
        this.value = val;
        this.next = next;
    }
}

class LinkedList{
    constructor(){
        this.head = null;
    }
    insertAtEnd(data){
        let node = new Node(data);
        if(!this.head){
            this.head = node;
            return this.head;
        }
        let tail = this.head;
        while(tail.next){
            tail = tail.next;
        }
        tail.next = node;
        return this.head;
    }
    insertAtbeginning(data){
        let node = new Node(data);
        node.next = this.head;
        this.head = node;
        return this.head;
    }
    insertAfter(previousNode, data){
        if(!previousNode){
            console.log('Please provide the details');
        }
        let node = new Node(data);
        let last = this.head;
        while(last){
            if(last.value === previousNode){
                node.next = last.next;
                last.next = node;
                break;
            }
            last = last.next;
        }
    }
    printList(){
        let temp = this.head;
        let formatList = 'Head :';
        if(!temp){
            console.log('Empty List');
            return;
        }
        while(temp){
            formatList = formatList + ' => ' + temp.value;
            temp = temp.next;
        }
        console.log(formatList);
    }
}

LinkedList.prototype.deleteStartNode = function() {
    if(!this.head){
        console.log('Nothing to delete'); 
        return ;
    }
    this.head = this.head.next;
    return this.head;
}

LinkedList.prototype.deleteLastNode = function() {
    if(!this.head){
        console.log('Nothing to delete'); 
        return ;
    }
    let previous = this.head;
    let tail = previous.next;
    if(!tail){
        this.head = null;
        console.log('Deleting the only left node');
        return;
    }
    while(tail.next){
        previous = tail;
        tail = tail.next;
    }
    previous.next = null;
    return this.head;
}
LinkedList.prototype.deleteNode = function deleteNode(node){
    if(!this.head){
        console.log('Nothing to delete'); 
        return ;
    }
    let previousNode = this.head;
    let currentNode = this.head;
    if(currentNode.value === node){
        console.log('Head is the Node to be deleted');
        this.head = currentNode.next;
        return;
    }
    
    while(currentNode){
        if(currentNode.value === node){
            previousNode.next = currentNode.next;
            return;
        }
        previousNode = currentNode;
        currentNode = currentNode.next;
    }
    if(!currentNode){
        console.log('There is no such node to delete');
    }

}
LinkedList.prototype.deleteNodeFromIndex = function(index){
    if(!this.head){
        console.log('Nothing to delete'); 
        return ;
    }
    let counter = 0;
    let currentNode = this.head;
    let previousNode = null;
    if(index === 0){
        this.head = currentNode.next;
        console.log('Head is the Node to be deleted');
        return;
    }
    while(currentNode){
        if(counter === index){
            previousNode.next = currentNode.next;
            return;
        }
        counter++;
        previousNode = currentNode;
        currentNode = currentNode.next;
    }
    if(!currentNode){
        console.log('List is shorter than given index');
    }
}
LinkedList.prototype.deleteList = function(){
    this.head = null;
}

let linkedListInst = new LinkedList();
linkedListInst.insertAtEnd(10);
linkedListInst.insertAtEnd(20);
linkedListInst.insertAtbeginning(40);
linkedListInst.insertAtbeginning(5);
linkedListInst.insertAfter(40, 50);
linkedListInst.printList();
linkedListInst.deleteStartNode();
linkedListInst.printList();
linkedListInst.deleteLastNode();
linkedListInst.printList();
linkedListInst.deleteNode(100);
linkedListInst.printList();
linkedListInst.deleteNode(40);
linkedListInst.printList();
linkedListInst.insertAtEnd(90);
linkedListInst.insertAtEnd(20);
linkedListInst.insertAtEnd(70);
linkedListInst.insertAtEnd(80);
linkedListInst.printList();
linkedListInst.deleteNodeFromIndex(9);
linkedListInst.deleteNodeFromIndex(2);
linkedListInst.printList();
linkedListInst.deleteNodeFromIndex(4);
linkedListInst.printList();
linkedListInst.deleteNodeFromIndex(0);
linkedListInst.printList();
linkedListInst.deleteNodeFromIndex(1);
linkedListInst.printList();
