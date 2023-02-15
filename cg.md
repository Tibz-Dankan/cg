#### describe open gl

OpenGL (Open Graphics Library) is a cross-platform graphics API (Application Programming Interface) that provides a standard interface for creating 2D and 3D graphics in computer applications. It was first introduced in 1992 and has since become one of the most widely used graphics APIs.

OpenGL is designed to be hardware-independent, meaning that it can be used on a wide range of computer systems, including desktop computers, game consoles, mobile devices, and embedded systems. It provides a set of functions and commands that allow developers to create 2D and 3D graphics, as well as perform various other tasks such as texture mapping, lighting, shading, and more.

OpenGL works by allowing developers to send commands and data to the graphics processing unit (GPU) in order to create and manipulate graphics. This allows for high performance and efficient use of hardware resources, making it a popular choice for creating real-time graphics in video games, scientific simulations, virtual reality, and other applications.

OpenGL is constantly evolving and has gone through several major revisions over the years. The most recent version is OpenGL 4.6, which was released in 2017 and includes many new features and enhancements, including improved performance, support for new hardware and operating systems, and more advanced graphics capabilities.

#### draw green square

```.cpp
#include <GL/glut.h>

void display() {
glClear(GL_COLOR_BUFFER_BIT); // Clear the screen
glColor3f(0.0, 1.0, 0.0); // Set color to green
glRectf(-0.5, -0.5, 0.5, 0.5); // Draw the square
glutSwapBuffers(); // Swap the front and back buffers (double buffering)
}

int main(int argc, char\*\* argv) {
glutInit(&argc, argv);
glutInitDisplayMode(GLUT_DOUBLE | GLUT_RGB);
glutInitWindowSize(400, 400);
glutCreateWindow("Green Square");

glMatrixMode(GL_PROJECTION);
glLoadIdentity();
glOrtho(-1, 1, -1, 1, -1, 1); // Set up a 2D orthographic projection matrix

glutDisplayFunc(display);
glutMainLoop();
return 0;
}
```

### translate square in x and y direction

To translate a square in the x and y directions, you can use the glTranslatef() function to apply a translation to the current matrix. Here's an example code snippet that shows how to translate a green square by (0.2, 0.3):

```.cpp

#include <GL/glut.h>

void display() {
glClear(GL_COLOR_BUFFER_BIT);
glLoadIdentity(); // Load the identity matrix

glTranslatef(0.2, 0.3, 0.0); // Translate by (0.2, 0.3, 0.0)
glColor3f(0.0, 1.0, 0.0);
glRectf(-0.5, -0.5, 0.5, 0.5);

glutSwapBuffers();
}

int main(int argc, char\*\* argv) {
glutInit(&argc, argv);
glutInitDisplayMode(GLUT_DOUBLE | GLUT_RGB);
glutInitWindowSize(400, 400);
glutCreateWindow("Translated Green Square");

glMatrixMode(GL_PROJECTION);
glLoadIdentity();
glOrtho(-1, 1, -1, 1, -1, 1);

glutDisplayFunc(display);
glutMainLoop();
return 0;
}

```

### rotate the square by 90 deg

To rotate the square by 90 degrees, you can use the glRotatef() function to apply a rotation to the current matrix. Here's an example code snippet that shows how to rotate a green square by 90 degrees:

```.ccp

#include <GL/glut.h>

void display() {
glClear(GL_COLOR_BUFFER_BIT);
glLoadIdentity(); // Load the identity matrix

glRotatef(90.0, 0.0, 0.0, 1.0); // Rotate by 90 degrees around the z-axis
glColor3f(0.0, 1.0, 0.0);
glRectf(-0.5, -0.5, 0.5, 0.5);

glutSwapBuffers();
}

int main(int argc, char\*\* argv) {
glutInit(&argc, argv);
glutInitDisplayMode(GLUT_DOUBLE | GLUT_RGB);
glutInitWindowSize(400, 400);
glutCreateWindow("Rotated Green Square");

glMatrixMode(GL_PROJECTION);
glLoadIdentity();
glOrtho(-1, 1, -1, 1, -1, 1);

glutDisplayFunc(display);
glutMainLoop();
return 0;
}

```

### rotate and scale the square

To rotate and scale the square, you can use the glRotatef() and glScalef() functions to apply rotations and scaling to the current matrix. Here's an example code snippet that shows how to rotate a green square by 45 degrees and scale it by a factor of 1.5:

```.cpp
#include <GL/glut.h>

void display() {
glClear(GL_COLOR_BUFFER_BIT);
glLoadIdentity(); // Load the identity matrix

glRotatef(45.0, 0.0, 0.0, 1.0); // Rotate by 45 degrees around the z-axis
glScalef(1.5, 1.5, 1.0); // Scale by a factor of 1.5 in the x and y directions
glColor3f(0.0, 1.0, 0.0);
glRectf(-0.5, -0.5, 0.5, 0.5);

glutSwapBuffers();
}

int main(int argc, char\*\* argv) {
glutInit(&argc, argv);
glutInitDisplayMode(GLUT_DOUBLE | GLUT_RGB);
glutInitWindowSize(400, 400);
glutCreateWindow("Rotated and Scaled Green Square");

glMatrixMode(GL_PROJECTION);
glLoadIdentity();
glOrtho(-1, 1, -1, 1, -1, 1);

glutDisplayFunc(display);
glutMainLoop();
return 0;
}
```

### scaling and rotation to the square

To apply scaling and rotation to the square, you can use the glRotatef() and glScalef() functions to apply rotations and scaling to the current matrix. Here's an example code snippet that shows how to rotate a green square by 45 degrees and scale it by a factor of 1.5 in the x direction and 0.5 in the y direction:

```.cpp
#include <GL/glut.h>

void display() {
glClear(GL_COLOR_BUFFER_BIT);
glLoadIdentity(); // Load the identity matrix

glRotatef(45.0, 0.0, 0.0, 1.0); // Rotate by 45 degrees around the z-axis
glScalef(1.5, 0.5, 1.0); // Scale by a factor of 1.5 in the x direction and 0.5 in the y direction
glColor3f(0.0, 1.0, 0.0);
glRectf(-0.5, -0.5, 0.5, 0.5);

glutSwapBuffers();
}

int main(int argc, char\*\* argv) {
glutInit(&argc, argv);
glutInitDisplayMode(GLUT_DOUBLE | GLUT_RGB);
glutInitWindowSize(400, 400);
glutCreateWindow("Scaled and Rotated Green Square");

glMatrixMode(GL_PROJECTION);
glLoadIdentity();
glOrtho(-1, 1, -1, 1, -1, 1);

glutDisplayFunc(display);
glutMainLoop();
return 0;
}

```
