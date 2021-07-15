//selectors

const todoInput = document.querySelector(".todo-input");
const todoButton = document.querySelector(".todo-button");
const todoList = document.querySelector(".todo-list");
const selectPriority =document.querySelector("#priority");


//priority-btns
const lowBtn = document.querySelector(".low-btn");
const mediumBtn = document.querySelector(".medium-btn");
const highBtn = document.querySelector(".high-btn");
const allBtn = document.querySelector(".all-btn");





//event listner
todoButton.addEventListener("click",addTodo);
todoList.addEventListener("click",deleteCheckPriority);

highBtn.addEventListener("click",filter);
mediumBtn.addEventListener("click",filter);
lowBtn.addEventListener("click",filter);
allBtn.addEventListener("click",filter);







//function

function addTodo(event){
    event.preventDefault();
    //TODO Div
    const todoDiv = document.createElement('div');
    todoDiv.classList.add("todo");

    //todo li
    const newTodo =document.createElement('li');
    newTodo.innerText= todoInput.value;
    newTodo.classList.add('newtodo');
    todoDiv.appendChild(newTodo);



    if(todoInput.value === ''){
        alert('Please name your Task');
    }else{



    // select priority
    const priority = document.createElement('div');
    priority.setAttribute("id", "priority-lable");
    priority.innerText= selectPriority.value;
    priority.classList.add(selectPriority.value);
    todoDiv.appendChild(priority);
    todoDiv.classList.add(selectPriority.value);



    if(selectPriority.value === 'none'){
        alert('Please select Priority');
    }else{



    //completed button 
    const completedBtn = document.createElement('button');
    completedBtn.classList.add('completed-btn');
    completedBtn.innerHTML= '<i class="fas fa-check"></i>';
    todoDiv.appendChild(completedBtn);



     //delete button 
    const deleteBtn = document.createElement('button');
    deleteBtn.classList.add('delete-btn');
    deleteBtn.innerHTML= '<i class="fas fa-trash"></i>';
    todoDiv.appendChild(deleteBtn);



    //append to list
    todoList.appendChild(todoDiv);

    //clearinput value
    todoInput.value='';


    };
    
    };  
    
}

 



function deleteCheckPriority(e){
    const item = e.target;
    //delete todo
    if (item.classList[0] === "delete-btn"){
        const todo = item.parentElement;
        //animation
        todo.classList.add("fall");
        //remove
        todo.addEventListener("transitionend",function(){
            todo.remove();
        });
        
    }

    //tick a task
    if (item.classList [0]=== "completed-btn"){
        const todo = item.parentElement;
        todo.classList.toggle('completed');
    }

 
}









// filter of priority

function filter(e){
    const todos = todoList.childNodes;
    todos.forEach(function(todo){
        switch(e.target.value){
            case "all":
                if(todo.classList.contains('todo')){
                    todo.style.display="flex";
                }else{
                    todo.style.display="none";
                }    
                break;

            case "low":
                if(todo.classList.contains('Low')){
                    todo.style.display="flex";
                }else{
                    todo.style.display="none";
                }    
                break;


            case "high":
                if(todo.classList.contains('High')){
                    todo.style.display="flex";
                }else{
                    todo.style.display="none";
                }
                break;

            
            case "medium":
                if(todo.classList.contains('Medium')){
                    todo.style.display="flex";
                }else{
                    todo.style.display="none";
                }    
                break;
                 

            
        }
    });
}


