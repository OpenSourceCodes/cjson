CJSON
=====

this is a library to make a compact json by decoupling the definition from data in a json object

* Example:


{ "EmployeeNumber": 23000, "EmployeeName" : "John Smith" }

{
"Names" : {"1":"EmployeeNumber", "2":"EmployeeName"},
"Data" : {"1" : 23000,"2" : "John Smith"}
}          


{
"Employee" : { "EmployeeNumber": 23000, "EmployeeName" : "John Smith" },
"Employee" : { "EmployeeNumber": 23000, "EmployeeName" : "John Smith" },
"Employee" : { "EmployeeNumber": 23000, "EmployeeName" : "John Smith" },
"Employee" : { "EmployeeNumber": 23000, "EmployeeName" : "John Smith" },
"Employee" : { "EmployeeNumber": 23000, "EmployeeName" : "John Smith" }
}

{
"Names" : {"1": "Employee", "2":"EmployeeNumber", "3":"EmployeeName"},
"Data" :
"1": {"2" : 23000, "3" : "John Smith" },
"1": {"2" : 23000, "3" : "John Smith" },
"1": {"2" : 23000, "3" : "John Smith" },
"1": {"2" : 23000, "3" : "John Smith" },
"1": {"2" : 23000, "3" : "John Smith" },
"1": {"2" : 23000, "3" : "John Smith" },
"1": {"2" : 23000, "3" : "John Smith" }
}          



{
"Names" : {"x1": "Employee", "x2":"EmployeeNumber", "x3":"EmployeeName"},
"Data" :
{"1": {"2" : 23000, "3" : "John Smith" },
"1": {"2" : 23000, "3" : "John Smith" },
"1": {"2" : 23000, "3" : "John Smith" },
"1": {"2" : 23000, "3" : "John Smith" },
"1": {"2" : 23000, "3" : "John Smith" },
"1": {"2" : 23000, "3" : "John Smith" },
"1": {"2" : 23000, "3" : "John Smith" }
}          

}




{
"Data2" : [
{
"x1": {"x2" : 23000, "x3" : "John Smith" } 
},
{
"x1": {"x2" : 23000, "x3" : "John Smith" } 
}
]          



public class X1
{
    public int x2 { get; set; }
    public string x3 { get; set; }
}

public class Data2
{
    public X1 x1 { get; set; }
}

public class RootObject
{
    public List<Data2> Data2 { get; set; }
}


