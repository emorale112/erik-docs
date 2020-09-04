Retrieve valid JSON for the product by invoking Retrieve Product Elements
Structure with the list of elements returned by Retrieve Elements. You will receive a JSON schema as a response.

The JSON schema represents the collection of elements needed to invoke the
product. The schema is populated with null values that you need to replace with
your own. For example, decision-collection.json represents the JSON schema for a
loan application. Automated Underwriting needs this schema in order to create an
underwriting decision for the loan application.


Step | Description
---------|----------
 1 | <p>Create a transaction by invoking **Create Transaction**. You will receive a *transaction_id* as a response.<br><br> A transaction in Staircase is an acknowledgement that you want to call a Staircase product, such as **Automated Underwriting**. It’s a container for everything associated with that product invocation, and is correlated with a collection related to the product (e.g. a loan application or a document). You need to create a new transaction every time you want to connect with a Staircase product. Staircase then associates everything, from a data and API execution standpoint, to that transaction.<br> 
 2 | <p>Understand what elements a product requires in a request by invoking **Retrieve Elements** You will receive a list of required elements as a response. <br><br> This is particularly useful for products that require a large payload for invocation. For example, **Automated Underwriting** requires, as part of the request, a loan application which in the MISMO model includes over 10,000 data elements. <br>
 3 | <p>Retrieve valid JSON for the product by invoking **Retrieve Product Elements Structure** with the list of elements returned by **Retrieve Elements**. You will receive a JSON schema as a response. <br><br> The JSON schema represents the collection of elements needed to invoke the product. The schema is populated with null values that you need to replace with your own. For example, [decision-collection.json](url) represents the JSON schema for a loan application. **Automated Underwriting** needs this schema in order to create an underwriting decision for the loan application. <br> 