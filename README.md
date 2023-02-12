
# Assignment 0

# Instuctions to build program

the program is build up using the visual studio 2019 IDE [you could you any even 2022 latest].

1. Select to build program:

Solution Configuration : Debug
Solution Platform : 64 

2. Got to Build -> Build Assignment It will build program. You will find Exe in Debug fodler of project directory

# Instruction to run program 

1. Go to the github link and download the project.
2. open project in Visual studio solution
3. Run program.

# Keys used:

O : for orthographic projection
P : for perspective projection(which is default one)

T - translate
S - scale
R - rotate

as per section of the above transaformation values [T/S/R keys]
you can use X, Y ,Z keys to translate, scale and rotate among all the axis

Escape: program will terminate.

# Description:


1. how screen is drawn?
==> We are rendering using OpenGL. You need something where you draw. 
In here it is "WINDOW" where you draw. Here window is drawn using GLFW library functions. The rendering is done using OpenGL APIs/functions.

2. how to draw object in the scene?
==> to draw objects in OpenGL first you need to create the data on CPU and then send it to GPU shader
steps:

a. first you write shader and compile those shaders. these shaders will get compiled on GPU.
b. link shader program object
c. then you store the data in vertex buffer objects and send it to GPU.
d. by using shader program object you will draw the objects on screen.

in code : vertex array objects and vertex buffer objects.

3. how do you make an object rotates?
==> to make objects rotation. OpenGL uses the maths here. here we use Open GLM library to perform these operation
It has an roation funtion which creates roatio matrix.

4. how do you make an object translates?
==> similar like above glm has translate function which creates translation matrix.

5. how do you make an object scales?
==> similar like above glm has scale function which creates scaling matrix.

By using above matrix we create transformationMatrix which make objects perform rotaion, translate, scale.


6. how to apply a texture on an object?
==> to apply text

7. how to make camera in perspective projection?
==> perspective projection means how does your eyes look basicaally. it has an pyaramid view. to set projection in OpenGL. you need projection matrix.
this matrix is crearted by using glm::perspective() function. then we will set it to shader via unifrom;

8. how to make camera in orthographic projections?
==> ortho means how dooes it look in 2D view. it had an cuboid view.
to create orthographic projection matrix. here we have used glm::ortho() function. which will create orthographic matrix for use.
Then we will send these to shader via uniform.

##############################################################

NOTE : TO UNDERSTAND THE DEATILS IN DEPTH YOU CAN CHECK OPENGL PIPELINE.
