# SMART Scopes v2 (work in progress)


## Why?
SMART is the _defacto_ authorization layer used by FHIR apps. Built on the widely deployed OAuth 2.0 authorization code flow, it tightly integrates FHIR resources with a launch extension. SMART's scope syntax has served us well, but is beginning to strain under the needs for finer grained control. For example, the `patient/Observation.read` scopes authorizes access to all [laboratory](https://www.hl7.org/fhir/codesystem-observation-category.html#observation-category-laboratory) results as well as the patient's [activity](https://www.hl7.org/fhir/codesystem-observation-category.html#observation-category-activity) (e.g. steps). 

## Goals
1) enhance SMART to scope operations
2) Provide ability to authorize types of categories of broad resources
3) Make simple, practical changes


## Principles
Machine-facing scopes should be different from consumer-facing scopes!
Scopes should sometimes be finer-grained than FHIR resources. 
Consumer-facing scopes should be simple and relatable.
Consumer-facing write scopes are special
Consumer authz requires info about the app, not just the data.


## Outstanding

1) What are existing production authorization scopes? 
