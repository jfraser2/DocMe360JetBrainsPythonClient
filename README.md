# DocMe360 Python Client

Reference Materials for Project<br/>
My Existing Code from other Projects and Assessments<br/>
Google, lol

#Run the Server Side in Eclipse(Do this first)
The server side project is in Git, it needs Docker Desktop to run.<br/>
The server side project name is: Joe-Fraser-DocMe360 and is loaded into Eclipse with<br/>
(File Import from Git) using url: https://github.com/jfraser2/Joe-Fraser-DocMe360.git<br/>
Follow all directions in the README.md<br/>

# Required Client Side Installs(Do this second)
open your fav Windows Shell Instance(Command Prompt Instance) as Administrator<br/>
Install Python, my version is 3.13.5, the install went to C:\Program Files\Python\Python313<br/>
Your folders may vary. lol<br/>
Additional installs with pip3 will go to folder C:\Program Files\Python\Python313\Lib\site-packages<br/>
pip3 install pydantic -U<br/>
pip3 install python-dateutil<br/>
pip3 install urllib3<br/>

#Load the Project on your Machine
Load the Project into JetBrains, any flavor, I used PyCharm<br/>
using url: https://github.com/jfraser2/DocMe360JetBrainsPythonClient.git<br/>
I think it will work in WebStorm, and even IntelliJ. The first load step is<br/>
under File, then choose Project from Version Control. Use the provided Url.<br/>
Next you will have to mark a lot of Folders. To start Right Click on the src folder<br/>
At the very bottom of the list you will see, Mark Directory as, then under that,<br/>
click Sources Root, the folder name should turn blue. The next top level folders to mark<br/>
are: forms, menus, openapi_client,  and panels. They are marked with Resource Root.<br/>
The marked folders will receive a very tiny orange-yellow three line icon. <br/>
The folder openapi_client has two children to mark, the same way: api and model<br/>
Now you have a project you can run. yea!! The true purpose is loading,<br/>
the behind the scenes file PYTHONPATH<br/>


#OpenApi Generator CLI(very Optional)<br/>
The source code in folder src/openapi_client was generated.<br/>
As always, I used the generate and fix methodology. lol <br/>
The files I had to repair were:<br/>
models/api_error.py<br/>
models/create_notification.py<br/>
models/update_template.py<br/>

Should you ever feel the need to re-gen the code, this is how you do it<br/>
Remember, you would have to re-apply the fixes in the three files listed above.<br/>
Open your fav administrator shell, then:<br/>
npm install @openapitools/openapi-generator-cli -g<br/>
if using the -g flag: Npm usually installs packages to the folder described below<br/>
macOS and Linux: Often found in /usr/local/lib/node_modules or a user-specific directory like ~/.npm-global.<br/> 
Windows: Typically located in %APPDATA%\npm\node_modules.<br/>
On my machine this is:<br/>
C:\Users\joe\AppData\Roaming\npm\node_modules<br/> 
to find the exact location type:<br/>
npm root -g<br/>

Run two commands in your fav administrator shell<br/>
cd to the project install folder.<br/>
openapi-generator-cli generate -i ./OpenApiConfig.json -g python -o ./src --additional-properties=generateSourceCodeOnly=true<br/>
 

#Run the client Side in JetBrains(Do this third)
In the src folder of the project, open app.py(double click on the name)<br/>
Then click the Run Icon, a Green Triangle, on the top Menu<br/>
After the GUI appears expand it to full size, and test away.<br/>
Even If you forget to start the Server, it will not bomb<br/>
 
You can also run it from the command line<br/>

#Example Command Line
open your fav Windows Shell Instance(Command Prompt Instance)<br/>
Then cd to the project Install folder<br/>
cd C:\work\AI\DocMe360JetBrainsPythonClient<br/>
"C:\Program Files\Python\Python313\python" ./src/app.py
