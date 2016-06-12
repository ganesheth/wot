# Problem Statement
Typically, (REST) resources are used with query parameters such as /resource?par1=value&par2=value... . How we are going to describe this in the TD for the different interactions such as properties, actions, and events? Static based query parameters are not the problem, however, dynamic based paramers have to be constructed at the time when a client setup the request. 

#Use Case
* function parameters
* OCF if views 
* filtering / selecting of, e.g., JSON or XML-based data (or Yang data)
* ...

#First Ideas
1)  define query parameters in the same way as the inputValue and outputValues
2) Use URI template and pre-processing similar to JSON Hyperschema proposal. Example:

{
	"name": "temperature",
	"inputType":{"properties":{"includTimestamp", type:"boolean"}}
	"href": "temp?inc_ts={includeTimestamp}"
}

Alternatively, we could adopt json hyperschema such links are part of the type itself.
