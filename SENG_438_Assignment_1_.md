## Course Title: Software Testing, Reliability, and Quality
## Course Code: SENG 438
## Assignment \#: 1
## Student Names:
    Aashik Ilangovan (30085993)
    Emmanuel Omari-Osei (30092729)
    Gibran Akmal (30094918)
    Priyanka Gautam (30091244)
## Group Number: 31
## Submission Date: 28/01/2022
## Space ID: aashik.blacklog.com

Introduction Software testing is the process of analyzing and evaluating
a software system with the intent of finding as many defects as possible
and/or gaining sufficient confidence in the software system under test.
There are several types of testing approaches, among which are
exploratory testing, manual scripted testing, and regression testing.

      In exploratory testing, tests are designed and executed at the same time. Exploratory testing is a refined form of Ad-hoc testing and testers design and execute the next test based on the result of the current step. Tests are 'realistic' scenarios that will cause the software to either fail or fulfill its mission. This approach is executed by a human tester who increases their knowledge of the system by exploring the application/software. Here tests are made by varying inputs and states. For example, a tester might vary input by testing for different input combinations, or testing for illegal/legal inputs. 
      
      In manual scripted testing, tests are first designed and recorded. Then they may be executed at a later time by either the same or a different tester. The script includes test cases and test steps that are documented and there is no deviation made by the tester from the path laid out in the script. 
      
      Regression testing is testing done to check that a system update did not reintroduce faults that have been corrected earlier. This testing is usually performed after someone has fixed a bug in the system.
      
    In this lab, we will be procuring an understanding of some fundamentals involved in testing through gaining hands-on experience in testing an example software system. This will aid us in further learning the differences between various testing approaches and help us familiarize ourselves with industrial defect tracking systems, processes and practices. 

High-Level Description Exploratory (Manual Non-Scripted) Functions being
targeted: Key user input functions in the program include card and pin
code interpretation and mathematical computations.

Approach and Justification: Test most functions a little bit because we
want to test the overall stability and structure of the system, and
examine their reliability. The reason we want to test a lot of functions
a little bit compared to testing a few functions extensively is that we
want to complete the flow of the program from start to finish and test
the different functions as we come across them instead of honing on a
few functions. In order for a system to flow smoothly, all of the
functions need to be operating properly at a basic level. Most basic
operations of the system should be functional. Detailed inspection of
exceptional issues can be scrutinized upon discovery.

Extensivity of Testing: Surface level testing will be performed to
ensure the program runs correctly with standard expected input. Testing
will not dive further past regular user input. This is to ensure the
operation is functional on regular use.

Development of Test Cases: We will test the most common paths for a user
using the ATM. For instance, a user using an ATM to withdraw cash or
deposit money. Common real-life experiences with ATMs will be used in
developing test cases. Comparison of Exploratory and Manual Functional
Testing (MFT) One key benefit to Scripted Testing is that it follows a
set path that has been designed and reviewed in advance. Since the
script includes well-documented test cases and test steps that, with no
deviation from the path laid out in the script, tests can be run in an
automated way. For example, when we were conducting the MFT testing in
the lab, since all of the tests in appendix C were well-documented with
the system's initial state, the function being tested and inputs, it was
easy for our team to run the tests on the system. Another benefit of MFT
is that there is little to no room for ambiguity in how the test cases
need to be run and executed.

      On the other hand, explanatory tests rely on the tester to develop the testing path 'on the go.' This is beneficial because although it's not exactly a testing 'free-for-all,' it allows the tester to go where an end-user might go rather than where a script tells them to go. Another benefit is that each tester will have different cases that they wish to test the system against, which might not have been thought about previously. Since each tester brings a new perspective about potential vulnerabilities of the system, they can detect bugs that were missed by the previous tester or a script that tests for the same use cases every time. For example, in this lab, our groups encountered different ideas about what to test for and so we caught a few bugs that were missed by the MFT test cases. 

      Both testing strategies have different uses in certain scenarios. Knowing when to use which strategy in which scenarios requires consideration of their respective tradeoffs. In the case of Scripted Testing, disadvantages stem from the rigidity of the scripted plan for testing. Testing is kept exclusively to the script, which can result in very little accommodation for deviation, even if other faulty areas of the system are observed. For example, in our lab, while conducting the exploratory testing, we noted a functionality error in the selection options that were part of the transaction menu. We reported this error in the backlog menu, and we hoped to see this error be further investigated by the MFT testing suite. However, we found that this error was not documented in the MFT test suite. Luckily, we had already encountered it in exploratory testing and logged the bug. This goes to show that if we had only been following the testing script, there would be undocumented/undiscovered bugs in the system. Additionally, since testing is merely a basic test of the product's overall functionality, non-basic tests are entirely ignored, regardless of the fact that their occurrence might be more frequent than the basic tests.

    With exploratory testing, there is little planning for the testing because this type of approach is mainly using a broad focus to find specific bugs. Due to this broad focus, one tradeoff for using this approach is that it can lead to many critical points of failure being overlooked or even missed. Also, the validity of the test is primarily justified by the experience of the tester. This can make testing from one end-user to another varied and produce mixed results, which may not favour verifying the program has been thoroughly tested. This point was clearly observed during our lab, where different testing pairs noted different issues in their exploratory testing, which was mainly due to the fact that each pair varied their respective approaches taken to test the system.
    The efficiency of scripted testing is high, as it is systematic and methodical. Being driven through a guideline eliminates wasted time because following a guideline provides a clear aim as to what and where to test. This results in a testing process that is smooth and quick to obtain an overall picture of the system's performance. When our team performed the scripted testing for the lab, we noticed a lot of overlap in our noted bugs, likely due to how straightforward this testing approach is. Most error sites documented in the test cases were able to be replicated and noted by both teams efficiently without any prior knowledge about the tests. However, due to the rigid nature of scripted testing, there is a likely possibility that errors and faults in the system could have been missed, resulting in a testing process that is only somewhat effective. This is because many bugs and issues in a system may appear at random in unexpected areas that are not taken into account in a guided scripted test. For example, in our exploratory test, we found that the ATM system was dispensing money anytime an incorrect menu option was made.  In a real-world ATM system, this type of error could be detrimental, and yet the scripted testing completely missed it.  
      The efficiency of the exploratory system is low but very open-ended and quick. This type of testing requires an abstract testing plan and is not very efficient in terms of testing the majority of the software functionality. However, exploratory testing is human-based meaning that testers will most likely test the main functionalities of the software and so it is quite effective in finding whether the software works as intended; however other less severe bugs are not found. For instance, during our lab, we noted some critical bugs in our manual scripted testing that involved transferring incorrect amounts of money between accounts. In a real-world ATM system, this type of error could be detrimental, and yet the exploratory testing completely missed it. Furthermore, MFT detected other really vulnerable parts of the system, such as in test cases 29, had not only incorrect amounts of money being transferred but also between wrong accounts. Moreover, in test case 14, while withdrawing money, the ATM was dispensing more money than requested even though the end-user only requested to withdraw $20. This type of error could be detrimental to a real-life ATM and a real end-user, and exploratory testing completely missed it. 

MFT found lots of buried functional defects that exploratory tests
missed. Exploratory testing is also more effective at representing what
use cases an actual user would take, so less time is wasted going
through other less important use cases. Exploratory testing is less
effective in terms of the thoroughness of test cases, whereas scripted
testing is more effective in detecting more functional defects/bugs. To
get the most effective test, one should apply both scripted and
exploratory testing to maximize the number of defects found.

Notes and Discussion Surrounding Peer-Reviews After examining each
pair's defect report and looking at the bugs documented by each group,
not only were common defects observed between both groups, but also
there were bugs found by one pair that the other pair had not detected.
This divided testing strategy displayed the importance of testing the
program with multiple testing teams, as it diversified perspectives
taken when testing. This ideology proved especially true for the
exploratory testing as both teams took a different angle on the
high-level testing description and applied it in their tests. Given each
pairs' unique outlook on the exploratory testing, each group discovered
new bugs that had not yet been found. For this testing approach, for
example, one group explored the Money Market account type, while the
other focused on the end user's illegal inputs. However, in MFT testing,
even though each pair followed the same testing suite, one pair found
bugs that the other pair had not discovered and vice versa. This is due
to the fact that "no two times of the system running are the same." Each
time a system runs, it might have different bugs depending on what
environment it is running in. The different types of environment that
could have impacted the MFT test suite are different operating systems,
the computer's storage space, and the memory available for the system.
How Pair Testing was Managed and How Teamwork was Divided Teamwork is a
fundamental core part of software testing. We split into groups of two
in this lab to conduct paired testing on the same software. Both pairs
implemented the same testing methods, allowing for a more comprehensive
test of the software system. Pair Testing was found to be more
beneficial to our learning, as it allowed us to hone a commonly used
software development technique. In this technique, one member does the
testing by running the ATM software and the other analyzes or reviews
the testing, reporting any bugs found.

      The members in the pairs switched roles so that both partners could get experience using the Backlog software, learn how to document issues and write defect descriptions.  Furthermore, working in a team allowed each group member to see certain testing problems from another's viewpoint, broadening their perspective. For example, during the exploratory testing phase, not every group member had the exact same idea for an exploratory testing approach. In order to resolve these disputes, we collaborated and devised the most strategic, efficient approach, which encompassed the different routes team members would have taken individually. 
      
    Teamwork is incredibly important in software development as "teamwork makes the dream work." Learning how to work in a team is imperative for engineers across all disciplines because it introduces them to varying new perspectives that only strengthen the final product. One of the key lessons that we learned about teamwork is that open communication, transparency and hard work are the foundations of any successful group. 
       

Difficulties, Challenges, and Lessons from the Lab Over the course of
this lab, there were some challenges that we had to face together as a
team.

      Upon starting this lab, even though our whole team had prior experience using ATMs, there was still some confusion about certain features simulated in the ATM program. The program only mimicked the functional operations of an ATM; it could not represent all of its operations in this simulated format. Thus, this meant we had to take extra time to understand the differences between a 'real life' ATM and the given ATM software. For example, when the ATM software is turned on, the user is asked to input the maximum amount of money the ATM can dispense. While it did take some time for the team to get acquainted with the ATM program, eventually, we figured out how to configure and operate this program as if it were a real-life ATM. Furthermore, given the extensive nature of the software testing approaches we implemented in this lab, our team gained a better understanding of how the program worked.

    This lab's more significant challenges and difficulties came from discerning what should and should not be counted as errors. As noted in lectures, we should test errors against the context of the program rather than being biased toward how we would want the program to be designed. Deciding which errors to include in the defect report fueled discussion amongst our group. Even so, these discussions concluded with much thoughtful consensus in our group. Since we were testing the program with more than one person, we were able to share our opinions. . It is important to stay impartial while conducting tests to avoid a biased report. 

    Another benefit of our cooperation as a team was being able to note errors in the program that other members missed or had not encountered. This emphasized the importance of "over the shoulder" testing, as it offered diverse perspectives on tests performed, resulting in a more comprehensive test. The more thorough our testing, the better it is for the program, as more undiscovered bugs are detected. These lessons will surely be remembered in future projects as it will serve to save project costs and impede the release of faulty programs. 

Comments/Feedback Overall, the lab detailed a simple yet insightful
experience in real-world testing. The experience induced a healthy
working environment that explored not only our previous knowledge of the
course material but more importantly our ability to cooperate in group
settings. We discovered in our first run-through of using backlog and
testing the application produced minor difficulties. (such as
deciphering the website and its utilities) However, going through the
lab we were able to quickly overcome such difficulties, turning it into
a smooth and informative session. An improvement that could be
implemented in the lab document itself would be the descriptions of the
test cases in Appendix C. The current descriptions, such as the initial
state of the system, have a lot of ambiguity which can cause students to
make false assumptions. An improvement here would be that the
descriptions of the test cases could be more clear and descriptive to
help eliminate any confusion when performing test cases. All in all, we
found this lab easy to follow and an excellent introduction to testing
software.
