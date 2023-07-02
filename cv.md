![alt text](
https://www.instagram.com/p/BjhKvVDl5PG6lWlBKdOjlgdZPNkuK45bqw8NdY0/?igshid=MTc4MmM1YmI2Ng==)
<h3>Nikita Korneichuk</h3>
<p><em>tel.:</em> +38-095-0195-03-85  <em>email:</em> korneichuk.nikita@gmail.com</p>
<h3>About Me: </h3>
<p>The main goal in the work and the main motivator to continue to study
something new for me is the implementation of interesting projects.
When writing a program, I always want to pay attention to the readability 
of the code, its simplicity and, at the same time, multifunctionality.
I like to use my knowledge to solve unusual problems that allow me to come up
with something new or improve the old.
While working in a team, I really like to discuss the tasks set for the team
and options for solving them, to be present at the code review.</p>
<h3>Skills: </h3>
<p>Markup and styling: HTML5 / CSS3</p>
<p>Programming languages: JavaScript / TypeScript</p>
<p>Frameworks: Angular / React</p>
<p>Back-End: Node.js</p>
<p>Version control system: GitHub</p>
<p>Testing: Jest</p>
<h3>Experience:</h3>
<p>Worked as Strong Junior Front-End Developer at Leo-Source.
In the work I used all the technologies listed above. Performed 
tasks related both to the visual correction of sites, and logic, tests.
</p>
English Level: B2
<h3>Code Example:</h3>
\```
<div class="tasksApp">
  <h2>ToDo List</h2>
  <div class="taskInput">
    <input type="text" placeholder="Add new task" #task>
    <button (click)="addTask(task.value)"> Add </button>
  </div>
  <task-list></task-list>
</div>

import { Component } from '@angular/core';
import {Store} from "@ngrx/store";

import { TasksActions } from "./store/tasks.actions";
import {Observable} from "rxjs";
import {TasksSelector} from "./store/tasks.selectors";

@Component({
selector: 'app-root',
templateUrl: './app.component.html',
styleUrls: ['./app.component.scss']
})

export class AppComponent {
title = 'ToDo';
tasks$: Observable<string[]>

constructor(
private store$: Store,
) {
this.tasks$ = this.store$.select(TasksSelector.tasks)

}

addTask(value: string) {
console.log(this.tasks$)
this.store$.dispatch(TasksActions.addTask({task: value}))
}

completeTask(value: any) {
console.log(value)
}

deleteTask(index: any) {
}
}

import { TestBed } from '@angular/core/testing';
import { AppComponent } from './app.component';

describe('AppComponent', () => {
beforeEach(async () => {
await TestBed.configureTestingModule({
declarations: [
AppComponent
],
}).compileComponents();
});

it('should create the app', () => {
const fixture = TestBed.createComponent(AppComponent);
const app = fixture.componentInstance;
expect(app).toBeTruthy();
});

it(`should have as title 'ToDo'`, () => {
const fixture = TestBed.createComponent(AppComponent);
const app = fixture.componentInstance;
expect(app.title).toEqual('ToDo');
});

it('should render title', () => {
const fixture = TestBed.createComponent(AppComponent);
fixture.detectChanges();
const compiled = fixture.nativeElement as HTMLElement;
expect(compiled.querySelector('.content span')?.textContent).toContain('ToDo app is running!');
});
});

.taskInput {
margin-bottom: 20px;
}

.tasksApp {
width: 90%;
height: 90%;
position: relative;
background-color: #ebefec;
border-radius: 10px;
display: flex;
flex-direction: column;
align-items: center;
margin: 20px;
}
\```