# ODP-IP_and_InclusionExclusion
Java implementation of the algorithms: IP, DP, ODP, ODP-IP, and InclusionExclusion

Exact Algorithms for "Complete Set Partitioning" (i.e., for "Coalition Structure Generation").

To download the project, click on the "Download ZIP" button. It will take a while to download the 6.5 MB file.

  - This code contains java implementations of the following algorithms: IP, ODP-IP, DP, ODP, and IDP (which is the size version of ODP). It also contains a java implementation of the Inclusion-Exclusion algorithm by Bjorklund et al [2009] 

  - For more on the optimization problem itself, or the algorithms, see: [Rahwan et al. An Exact Algorithm for Complete Set Paritioning, 2014] and [Bjorklund et al. Set Partitioning via Inclusion-Exclusion, 2009]

  - The two main, executable java classes are the following (both come with a graphical user interface (GUI)):

      - SolveRandomProblems.java: This allows the user to experiment with the different algorithms with randomly-generated problem instances.

      - SolverParticularProblem.java: This allows the user to solver a particular problem, where the values of different coalitions (i.e., subsets) are stored in a file. Below are more details on the format of the file.

  - file format:
      - if you want to read the subset values from a file, it should be stored in a text file, where every line contains the value of one subset. Here is an example for the contnt of such a file, given 4 agents (i.e., 4 elements):

0\\
30
40
50
25
60
55
90
45
80
70
120
80
100
115
140

In a file containing values just like the above, the value in line x represents the value of the subset that is represented by the true bits in the number (x-1).

For example, assume we have the following four agents (or elements): {a1,a2,a3,a4}. The value at line 6 is 60 (see above). This represents the value of the subset that is represented by the true bits in number (6-1), which is: 0101. This subset is: {a1,a3}. Based on this, the above list of values represent the following problem:

0	is the value of the subset represented by	0 = 0000	which is {}
30	is the value of the subset represented by	1 = 0001	which is {a1}
40	is the value of the subset represented by	2 = 0010	which is {a2}
50	is the value of the subset represented by	3 = 0011	which is {a1,a2}
25	is the value of the subset represented by	4 = 0100	which is {a3}
60	is the value of the subset represented by	5 = 0101	which is {a1,a3}
55	is the value of the subset represented by	6 = 0110	which is {a2,a3}
90	is the value of the subset represented by	7 = 0111	which is {a1,a2,a3}
45	is the value of the subset represented by	8 = 1000	which is {a4}
80	is the value of the subset represented by	9 = 1001	which is {a1,a4}
70	is the value of the subset represented by	10 = 1010	which is {a2,a4}
120	is the value of the subset represented by	11 = 1011	which is {a1,a2,a4}
80	is the value of the subset represented by	12 = 1100	which is {a3,a4}
100	is the value of the subset represented by	13 = 1101	which is {a1,a3,a4}
115	is the value of the subset represented by	14 = 1110	which is {a2,a3,a4}
140	is the value of the subset represented by	15 = 1111	which is {a1,a2,a3,a4}

The optimal solution to this problem is the following partition: {{a1}, {a2}, {a3,a4}}. The value of this partition is: v({a1})+v({a2})+v({a3,a4}) = 150

License: All source files are made available under the terms of the GNU General Public License (GPL).
