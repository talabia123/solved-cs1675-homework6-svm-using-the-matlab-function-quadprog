Download Link: https://assignmentchef.com/product/solved-cs1675-homework6-svm-using-the-matlab-function-quadprog
<br>
In this assignment, you will implement an SVM using the Matlab function <span style="font-family: courier new;">quadprog</span>. The most useful resource are the handwritten notes and <b>the recitation on Oct. 26</b>.

<u>Part I: SVM via quadratic programming</u> (20 points)

Examine the Matlab function <a href="https://www.mathworks.com/help/optim/ug/quadprog.html"><span style="font-family: courier new;">quadprog</span></a>. It can be used train an SVM (find the optimal <b>w</b>). Consider the input variables <span style="font-family: courier new;">H,f,A,b,Aeq,beq,lb,ub</span>. How should you set each of them so that the quadratic program that is solved is the solution to an SVM? How would you compute the weight vector <b>w</b> from the output of <span style="font-family: courier new;">quadprog</span>?

With these answers in hand, your next task is to implement an SVM using a call to <span style="font-family: courier new;">quadprog</span> with appropriately set input parameters. Write a <span style="font-family: courier new;">function [y_pred] = svm_quadprog(X_train, Y_train, X_test, C)</span> that “trains” an SVM i.e. obtains the solutions for the alpha weights using <span style="font-family: courier new;">quadprog</span>, then computes the weight vector <i><b>w</b></i> from these. It should also compute a prediction on the test set, using the test features and the weight vector.The inputs to this function are:

<ul>

 <li>an NxD feature matrix <span style="font-family: courier new;">X_train</span> where N is the number of training instances and D is the feature dimension,</li>

 <li>an Nx1 label vector <span style="font-family: courier new;">y_train</span> for the training instances,</li>

 <li>an MxD feature matrix <span style="font-family: courier new;">X_test</span> where M is the number of test instances, and</li>

 <li>a scalar <span style="font-family: courier new;">C</span>, denoting the misclassification cost in an SVM.</li>

</ul>

The output is:

<ul>

 <li>an Mx1 predicted label vector <span style="font-family: courier new;">y_pred</span> for the test instances.</li>

</ul>

<u>Part II: Testing your SVM</u> (10 points)

Now test your SVM on the Pima Indians dataset from HW4. Reuse your KNN test script, but instead of testing different values of K or the bandwidth, test different values of C (e.g. 0.0001, 0.001, 0.01, 0.1, and 1). Name your adapted script <span style="font-family: courier new;">svm_classification.m</span>. Plot the performance of your SVM with the values of C on the x-axis, and the corresponding accuracies on the y-axis. Include the figure in a report file.

Important: Make sure to convert the ground-truth labels of 0 to -1. Then your predicted values should also be only -1 or 1.

<b>Submission:</b> Please include the following files:

<ul>

 <li><span style="font-family: courier new;">svm_quadprog.m</span></li>

 <li><span style="font-family: courier new;">svm_classification.m</span></li>

 <li><span style="font-family: courier new;">report.pdf</span></li>

</ul>