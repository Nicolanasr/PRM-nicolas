# Project Management Website for teams

Prm website built with django 3.1.7 and Python 3.9.1  
<a href="https://nicolas-prm-2.herokuapp.com/" target="_blank">Live Demo</a>  
[![Account Password change](https://img.shields.io/website?url=https%3A%2F%2Fnicolas-e-commerce.herokuapp.com%2Fstore%2F )](https://nicolas-prm-2.herokuapp.com/)   
<hr>

#### Landing Page
This is the first page a visitor will see. No one can access the groups pages before being assigned to a group.   
The users will be divided into groups and each group has a group leader (TL).   


<caption>Example:</caption>
<table>
<tr>
    <th colspan=3 style="text-align:center;">Admin</th>
</tr>
<tr>
    <th>group1</th>
    <th>group2</th>
    <th>group3</th>
</tr>
<tr>
    <th>group1TL</th>
    <th>group2TL</th>
    <th>group3TL</th>
</tr>
<tr>
    <td>group1User1</td>
    <td>group2User1</td>
    <td>group3User1</td>
</tr>
<tr>
    <td>group1User2</td>
    <td>group2User2</td>
    <td>group3User2</td>
</tr>
</table>




<img src="https://i.imgur.com/jwu2upo.png" alt="Landing Page" style="width:100%"/>  


#### Registration and login  
Each user will be able to login with their account if they have one Check <a href="#credentials">the end</a> for some usernames and passwords that you can use for testing) or register a new account, in this case they will have to wait until the admin assign them to a group.  


<img src="https://i.imgur.com/sZa3I91.png" alt="Login/signup" style="width:100%"/>  
<img src="https://i.imgur.com/doeNvEj.png" alt="Login/signup" style="width:100%"/>  

#### Tasks
Each user can only see the tasks assigned to their group (Who is the task assigned to, the due date, the status of the task).  
The task wil be highlighted for the user who the task is assigned to.   
If the task due date has already passed, a red triangle (overdue) will be shown next to the date.  
When a user gets assigned to a new task it will show in the notifications in the top right (The notification will automatically be deleted when the user clicks on it or click on the task).

<img src="https://i.imgur.com/mpF0Bqz.png" alt="Tasks Page" style="width:100%"/>  

If the user tries to access another groups page they will be redirected with an error  

<img src="https://i.imgur.com/jFdIoTx.png" alt="Tasks Page" style="width:100%"/>  

##### Adding a new task
If the logged in user is a TL (Group leader), they can <a href="#review">Review</a> or add new tasks.  

<img src="https://i.imgur.com/41kFf9u.png" alt="New Task" style="width:100%"/>  
  
The TL can only assign users that are apart of their group and will need to enter his/her password to confirm to add the task (The password confirmation is also required when <a href="#delete">Deleting</a> or <a href="#update">Updating</a> a task).  

<img src="https://i.imgur.com/rpYhLUW.png" alt="New Task" style="width:100%"/>  

##### Task page
The task page contains more info about a certain page plus anyone can comment on the task.  
Only the TL can edit or delete a task.   

<img src="https://i.imgur.com/clb9HUG.png" alt="Task page" style="width:100%"/>  

<strong id="update">Edit Task:</strong>  
<img src="https://i.imgur.com/0F79odE.png" alt="Task edit" style="width:100%"/>  
<strong id="delete">Delete Task:</strong>  
<img src="https://i.imgur.com/eT21yaT.png" alt="Task delete" style="width:100%"/>

###### A confirmation password is needed to either delete or update a task
<br>

If the user that is viewing the task page is assigned to that task, they will be able to mark it as done (The task Status will change from 'Active' to <a href="#review">Awaiting Review</a>) Or simply undone which will change it's status back to 'Active'.  

<img src="https://i.imgur.com/vKuMlwB.png" alt="Task Done" style="width:100%"/>  
<img src="https://i.imgur.com/vZdnOsf.png" alt="Task unDone" style="width:100%"/>  



<span id="review"></span>

##### Task Review:
The TL will be able to access the tasks that are awaiting review from the top right of the navbar and then access the task page to either edit it (Mark it as done or assign it back to the same or another user; They will get notified for either) or delete the task completely.

<img src="https://i.imgur.com/I3rIM9T.png" alt="Task review" style="width:100%"/>  
<img src="https://i.imgur.com/clb9HUG.png" alt="Task review" style="width:100%"/>  

<br><br><br>
<img src="https://i.imgur.com/4fSglPj.png" alt="Task review" style="width:100%"/>  
<hr>

<br>

# Installation
<ul>
<li>Clone or download the repository</li>
<li>CD into the folder that contains manage.py </li>
<li><code>pip install -r requirements.txt</code></li>
<li>Run <code>py manage.py runserver</code></li>
</ul>

<span id="credentials"></span>
## Login credentials for you to user to access and test the <a href="https://nicolas-prm-2.herokuapp.com/login" target="_blank">website</a>:
###### (All the changes made to the databases will automatically reset within 24 hrs so don't worry about messing things up)  
<br>
<table>
<tr>
    <th>Username:</th>
    <th>Password:</th>
    <th>Role/Group</th>
</tr>
<tr>
    <th>Teamleader_group1</th>
    <td>group1tl</td>
    <td>TL/group1</td>
</tr>
<tr>
    <td>usertest_group1</td>
    <td>testuser</td>
    <td>user/group1</td>
</tr>
<tr>
    <td>usertest2_group1</td>
    <td>testuser</td>
    <td>user/group1</td>
</tr>
<tr>
    <td>usertest3_group1</td>
    <td>testuser</td>
    <td>user/group1</td>
</tr>
<tr>
    <th>Teamleader_group2</th>
    <td>group2tl</td>
    <td>TL/group2</td>
</tr>
<tr>
    <td>usertest_group2</td>
    <td>testuser</td>
    <td>user/group2</td>
</tr>
<tr>
    <td>usertest2_group2</td>
    <td>testuser</td>
    <td>user/group2</td>
</tr>
</table>

<br>

<!-- login credentials: 
username: Teamleader_group1, password: `group1tl`
username: usertest_group1, password: testuser
username: usertest2_group1, password: testuser
username: usertest3_group1, password: testuser


username: Teamleader_group2, password: group2tl
username: usertest_group2, password: testuser
username: usertest2_group2, password: testuser -->