# Chapter 2 Entity-Relationship Model

## E-R Diagram Basics
---

### 1. Entity and Entity Set
**Entity**: An object
-   have attributes

**Entity set**: A set of entities of the same type that share the same attributes.

**E-R Diagram:**
-   Rectangle: entity set
-   Ellipse: attribute
-   Line between Rectangle and Ellipse: link between an entity and the an attribute

### 2. Relationship and Relationship Set
**Relationship**: an association among entities

**Relationship Set**: a set of relationships of the same type

**E-R Diagram:**
-   Diamonds: Relationship sets

### 3. Constraints
**Mapping cardinalities**
-   how many entities can be associated with another entities via a relationship set? *One or More than One?*
-   *E-R Diagram:*
    -   One: Directed line $$\rightarrow$$
    -   More than one: Undirected line $$-$$

**Participation constrainst**
-   how many entities in the entity set have to participate in the relationship set
    -   **Total Participation**: Every entity in the entity set participates in at least one relationship in the relationship set
    -   **Partial Participation**: Some entity may not participate in any relationship in the relationship set
-   *E-R Diagram:*
    -   Total Participation: Double line $$=$$
    -   Partial Participation: Single line $$-$$
  
### 4. Keys of an entity set
**Super Key**
-   A set of attributes whose values uniquely determine each entity

**Candidate Key**
-   A minimal supper key such that no subset of a candidate key is still a super key

**Primary Key**
-   The selected candidate key
-   *E-R Diagram:*
    -   Primary key is *underlined*: <u>attribute</u>

### 5. Attributes types

**Single-valued v.s. Multi-valued attributes**
-   Multi-valued attribute: accept more than one value
    -   *E-R Diagram*: double ellipses

**Derived attribute**
-   Values can be derived from other
attributes
    -    *E-R Diagram*: dashed ellipses

### 6. Weak Entity Set
**Weak entity set**: an entity set <u>without a primary key</u>

**Identifying entity set**: a weak entity set must relate to its identifying entity set via a **total, many-to-one** *identifying relationship set <u>from</u> the former <u>to</u> the latter*

**Discriminator** (or partial key): a set of attributes that distinguish among the weak
entities that depend on the same identifying entity.

### 7. Role
-   Specify how a subset of entities interact with another subset of entities
    -   Entity sets of a relationship need not be distinct

### 8. Specialization and Generalization
**Specialization**
-   designate sub-groupings within an entity set that are
distinctive from other entities in the set
-   A lower-level entity set inherits all
attributes and relationship set
participation of the higher-level
entity set to which it is linked
-   Lower-level entity set can have its
own attributes

**Total or Partial**
-   Specifies whether an entity in the higher level-entity set
must belong to at least one of the lower-level entity sets
within a specialization.

**Disjoint or overlapping**
-   Constraints on whether entities may belong to more than
one lower-level entity set within a single specialization.
    -   Disjoint: must be either A or B
    -   Overlapping: Can be both
-   *E-R Diagram*
    -   A disjoint specialization: "Disjoint" beside the "IS A"
    -   An overlapping specialization: Null, default