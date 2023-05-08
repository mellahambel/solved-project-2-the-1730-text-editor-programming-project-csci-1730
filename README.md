Download Link: https://assignmentchef.com/product/solved-project-2-the-1730-text-editor-programming-project-csci-1730
<br>
<h1>1           Problem / Exercise</h1>

Your goal is to implement a basic text editor, 1730ed, in C++ using system calls (APUE Ch. 3) for low-level file I/O and the ncurses library for the Text User Interface (TUI). This will require you to lookup things related to ncurses and apply your knowledge of object oriented programming.

Part of software development is being given a goal but not necessarily being given instruction on all of the details needed to accomplish that goal. For example, even though the ncurses library has not been covered in class, in order to complete this project you are going to need to lookup how to create TUIs using ncurses. To help make things a little easier, you and your partner may pick and choose the best parts of each other’s labs 4 and 5 to serve as a foundation for this project. Furthermore, since ncurses is a C library (and not a C++ library), you are going to need to take special care that you are still using C++ best practices and exercising concepts related to object oriented programming. For example, you may wish to create multiple classes in order to better organize your code base.

By submitting this project, you agree to the Academic Honesty policy as outlined in the course syllabus.

<h1>2           Functional Requirements (80 points)</h1>

Your submission needs to satisfy the following functional requirements:

<ul>

 <li><strong>Editor TUI (40 points): </strong>In addition to the editable text area, the main editor window needs to include text for the menu, the title, and the name of the file currently open in the editor. Here is an example of what the user interface might look like:</li>

 <li><strong>F1 Menu (20 points): </strong>If the user presses the F1 key (or fn-F1 on a Mac), then your editor needs to create a window somewhere in the terminal screen that allows the user to select from the following options:

  <ul>

   <li><em>Open: </em>This option should prompt the user to enter in a filename. After the user presses return/enter, your editor should attempt to open the file for editing. If an unsaved file is open in the editor when the user chooses this option, then your editor needs to ask the user whether or not they want to save their changes before opening the other file.</li>

   <li><em>Save: </em>This option should attempt to save the file currently open in the editor. The mode of the file should not be changed by your editor.</li>

   <li><em>Save As: </em>This option should prompt the user to enter in a new filename and attempt to save the file currently open in the editor to that new filename. If the file already exists, then your editor should ask the user if they want to overwrite the existing file.</li>

   <li><em>Exit: </em>This option should exit your editor. If an unsaved file is open in the editor when the user chooses this option, then your editor needs to ask the user whether or not they want to save their changes before exiting.</li>

  </ul></li>

</ul>

Feel free to add and implement other options, if you wish. Here is an example of what the menu might look like:

<ul>

 <li><strong>Display Errors (20 points): </strong>If a system call issues an error, then you your editor needs to create a window in the center of the terminal screen that displays that error. Whenever it makes sense to do so, your editor should prompt the user in an attempt to fix the problem. For example, if the open system call issues an error about a file not existing, then you might prompt the user to re-enter the filename.</li>

</ul>

<h1>3           Extra Credit Requirements (10 points)</h1>

You may gain some extra credit points if your submission includes the following:

<ul>

 <li><strong>Padded Line Numbers (5 points): </strong>Your editor should include line numbers on the left side of the TUI. These should be padded so that the text from the file that is open does not directly touch the numbers. If the user scrolls up or down, the line numbers should be adjusted accordingly.</li>

 <li><strong>Add Multiple Colors to your TUI (5 points): </strong>Make your editor colorful for users who are using a terminal emulator that supports colors. Try not to use colors that unfriendly to users who are color blind or who suffer from epilepsy.</li>

</ul>

<h1>4           Nonfunctional Requirements (20 points)</h1>

Your submission needs to satisfy the following functional requirements:

<ul>

 <li><strong>Directory Setup: </strong>Make sure that all of your files are in a directory called LastNameA-LastNameB-p2, where LastNameA and LastNameB are replaced with the actual last names of you and your pair programming partner.</li>

 <li><strong>Libraries: </strong>You are allowed to use any of the C or C++ standard libraries. The only third-party libraries you are allowed to use are ncurses-6.0 and any libraries that come bundled with ncurses-6.0. Failure to adhere to this non-functional requirement will result in an automatic 50 point deduction.</li>

 <li><strong>Documentation (5 points): </strong>All classes, structs, and functions must be documented using Javadoc (or Doxygen) style comments. Use inline documentation, as needed, to explain ambiguous or tricky parts of your code.</li>

 <li>Makefile <strong>File (5 points): </strong>You need to include a Makefile. Your Makefile needs to compile and link separately. That is, make sure that your Makefile is setup so that your .cpp files each compile to individual .o This is very important. The resulting executable should be called 1730ed.</li>

 <li><strong>Standards &amp; Flags (5 points): </strong>Make sure that when you compile, you pass the following options to g++ in addition to the -c option:</li>

</ul>

-Wall -std=c++14 -g -O0 -pedantic-errors

Other compiler/linker options may be needed in addition to the ones mentioned above. The expectation is that the grader should be able to type in the following to clean, compile, link, and run your submission:

$ make clean

$ make

$ ./1730ed somefile

<ul>

 <li>README <strong>File (5 points): </strong>Make sure to include a README file that includes the following information presented in a reasonably formatted way:

  <ul>

   <li>Your Name and 810/811#</li>

   <li>Instructions on how to compile and run your program.</li>

  </ul></li>

</ul>

Make sure that each line in your README file does not exceed 80 characters. Do not assume line-wrapping. Please manually insert a line break if a line exceeds 80 characters.

<ul>

 <li><strong>Compiler Warnings: </strong>Since you should be compiling with both the -Wall and -pedantic-errors options, your code is expected to compile without g++ issuing any warnings. Failure to adhere to this non-functional requirement will result in an automatic 5 point deduction.</li>

 <li><strong>Memory Leaks: </strong>Since this project may make use of dynamic memory allocation, you are expected to ensure that your project implementation does not result in any memory leaks. We will test for memory leaks using the valgrind Failure to adhere to this non-functional requirement will result in an automatic 5 point deduction.</li>

</ul>


