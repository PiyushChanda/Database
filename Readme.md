
Any Raw Value is Data
Any meaningful processed data is information

A Single item can be an information as well as data depending on the observer

Disadvantage of File Processing System - Data redundancy, consistency, security, transaction support

OLAP - Online Analytical Processing - Historical Data
OLTP - Online Transaction Processing - Current Data

ER Model
~~~~~~~~

Entity - An object that can be differentiated from other object with the help of same properties or attributes
Attributes - Quantifiable Property of an Entity

Conceptual non-technical representation

Entity Set - Set of similar entities

Relationship - Assossiation between two or more entities is called a relationship
Relationship Set - Set og similar relationships

Types of Attributes - Simple or Composite, Single or Multivalued, Stored or Derived

Degree - Number of entities taking part in a relationship

Cardinality - It specified how many entities of an entity set can take part in a relationship
1 - 1
1 - m
m - 1
m - n

1 - m - Atmost 1 entity can be related with m entities

Participation Constraints - How many entites can be assossiate through a relationship

Functional Dependency - One attribute uniquely identifies another attribute

Armstrong's Axioms
~~~~~~~~~~~~~~~~~~
AB Identifies A
A Identifies B, implies AC identifies BC
A Identifies B, and B identifies C, then A identifies C

A Identifies B, and A Identifies C, then A identifies BC, and Vice Versa
A Identifies B, and WB Identifies X, then WA identifies X
A Identifies B, and C Identifies D, then AC identifies BD

Closure of A - All the attributes that can be directly or indirectly identified by A

If the closure of Attributes are same for two functional dependency, then we can say that the two dependency sets are equal

When we remove the redundant element, that is, when we remove the element whose presence
doesnot affect the closure of the dependecy set, then we are left with minimal dependency set or cannonical cover

Super Key - The closure of which is the whole set of attributes
Candidate Key - When we remove the element from super key that is not responsible for it's uniqueness
then we get a candidate key, whose proper subset cannot be a super key, minimal super key is called candidate key

Redundancy - When same piece of information is copied in multiple locations in a file
Insertion Anomaly - When data cannot be inserted without some other assossiated data
Updation Anomaly - When the same set of information needs to be updated multiple times
Deletion Anomaly - When deletion of unwanted data causes deletion of wanted data

1 NF - Atomic Values
2 NF - No partial dependencies - i.e. a prime attribute (proper subset of candidate key) should not identify a non-prime
attribute
3 NF - No transitive dependencies - i.e. a non-prime attribute should not identify a non-prime attribute

i.e. if a - b exits then for the table to be in 3NF we need to check
1. b is prime
2. a is super key
if either a or b holds, that dependency holds good

BCNF - a - b holds, then a must be a super key, there may be a loss of dependency while decomposing a 3 NF to BCNF

A join is lossless if we get the original information after combining the associated tables.

1. We must get the original set of attributes
2. There must be one common key, and one of which should be a candidate key, also intersection of two decomposed relation
must not be null

Dependency Preserving decomposition - If decomposition results in preservation of dependency

Indexing
1. Value - Block Number





