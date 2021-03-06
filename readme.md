This program is designed to give management teams an
empirical data point to consider in
deciding on just compensation for an internal
candidate being considered for a promotion.
Slightly adapted, it is also a way to semi-anonymously
and democratically gauge an employee's performance.

The software prompts an administrator to set up the
ballot, then elicits responses from a number
of reviewers (voters) who have worked with the colleague
up for promotion (and therefore have some insight into
their reliability, the quality of their work, etc).
The voters submit what they feel the candidate should
make in their new role; the inputs are averaged (i.e.
anonymized) and provided to the management team, for
them to incorporate into their decision-making process
as the group's perceived value of the candidate.

// Below are ideas for further development:

In order to preserve anonymity but to maintain a record
of the data inputs, a mechanism could be included that builds
a crowd-composed password that is used to encrypt part of the
file written that includes data of all their inputs.
This would ensure that only by unanimous consent (i.e. all
users provide their accurate password segments) can the
complete password be re-composed to decrypt
the inputs (votes) - to 'semi-unanonymize' them. (Or
should that file have names affiliated with voted salaries?)

The goal - initially - is to provide organizational
managers more insight into the perceived value an
employee brings to the effort. Perhaps this employee
flies under the radar but consistently and reliably
delivers high quality work for colleagues, or is a
brown noser who management likes but who doesn't actually
deliver on the tasks. In both cases, management may
misperceive the candidate's value to the organization
and make an offer mis-aligned to the candidate's
true contribution.

Eventually I am interested in designing an organization
governed by code - smart contracts - that leverages
a voting system in which any worker's experience
and value (as perceived by the group) influence
the weight of their votes on decision-making,
from strategic direction to operational and
hiring decisions, etc.


For this iteration we define three classes - a 'voter'
class, a 'candidate' class and a 'manager' class.

Managers input the number of voters and the names of
the candidates, then are asked to leave the terminal.
(All of this takes place in one interface - an opportunity
for biometric identification to verify that each person is
who they are saying they are ? )

First, an administrator (maybe the manager who will
receive the final output) creates a vector of candidate
objects. Each voter will then input whether they feel
the candidate should be promoted (bool) and what they
feel that candidate's salary should be (int), values
recorded in the candidate's 'suggested_salaries' and
'promote' vectors.

Voters are also asked to provide a 5 character passcode,
to be used to build a collective password used to
encrypt each voter's inputs in a manner that can only
be decrypted (for review, for example) if every voter
consents by providing the 5 characters. These encrypted
inputs will be written to a file.

Once all voters have voted the program will display
a single float value for the eyes of the
management team: the average suggested salary as
collected from the team that worked with the
candidate.
