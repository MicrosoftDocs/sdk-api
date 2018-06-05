---
UID: NN:msopc.IOpcRelationshipSelector
title: IOpcRelationshipSelector
author: windows-sdk-content
description: Represents how to select, from a Relationships part, the relationships to be referenced for signing.
old-location: opc\iopcrelationshipselector.htm
old-project: OPC
ms.assetid: 077f37c3-76af-4b96-9e3a-9fd9b865d941
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: IOpcRelationshipSelector, IOpcRelationshipSelector interface [Open Packaging Conventions], IOpcRelationshipSelector interface [Open Packaging Conventions],described, msopc/IOpcRelationshipSelector, opc.iopcrelationshipselector
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msopc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: OPC_SIGNATURE_TIME_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msopc.h
api_name:
-	IOpcRelationshipSelector
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcRelationshipSelector interface


## -description


Represents how to select, from a Relationships part, the relationships to be referenced for signing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcRelationshipSelector</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpcRelationshipSelector</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcRelationshipSelector</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac1f0347-9b89-4d8f-b0cb-14708e7a6e55">GetSelectionCriterion</a>
</td>
<td align="left" width="63%">
Gets a string that is used to select relationships to be referenced for signing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/583f56e5-c374-4f79-badd-35eb5eecef70">GetSelectorType</a>
</td>
<td align="left" width="63%">
Gets a value that describes how relationships are selected to be referenced for signing.

</td>
</tr>
</table> 


## -remarks



To create an 
				 <b>IOpcRelationshipSelector</b> interface pointer, call the <a href="https://msdn.microsoft.com/801d1924-c75c-47b5-99fe-9d97ea8dfee1">IOpcRelationshipSelectorSet::Create</a> method.

To access an <b>IOpcRelationshipSelector</b>, call the <a href="https://msdn.microsoft.com/ffff6b7e-8e46-4be6-921f-b98e7d51a114">IOpcRelationshipSelectorEnumerator::GetCurrent</a> method.

Use the <b>IOpcRelationshipSelector</b> interface methods to select relationships for signing. A relationship is selected if its type or identifier matches the string that is retrieved by calling the <a href="https://msdn.microsoft.com/ac1f0347-9b89-4d8f-b0cb-14708e7a6e55">GetSelectionCriterion</a> method. This string is either a relationship type or a relationship identifier.  Call the <a href="https://msdn.microsoft.com/583f56e5-c374-4f79-badd-35eb5eecef70">GetSelectorType</a> method to get an <a href="https://msdn.microsoft.com/5532aab1-850e-4de8-a470-c55fb4c2f8c4">OPC_RELATIONSHIP_SELECTOR</a> value to determine whether the string is a relationship type or an identifier. To access these relationship properties, call the <a href="https://msdn.microsoft.com/da832c8e-99e1-452a-90eb-97580f00f003">IOpcRelationship::GetRelationshipType</a> and <a href="https://msdn.microsoft.com/8646d592-d568-4b82-80f3-2673cd0d2721">IOpcRelationship::GetId</a> methods.

The following table shows how <a href="https://msdn.microsoft.com/5532aab1-850e-4de8-a470-c55fb4c2f8c4">OPC_RELATIONSHIP_SELECTOR</a> values map to the relationship type and relationship identifier properties.<table>
<tr>
<th>
<a href="https://msdn.microsoft.com/5532aab1-850e-4de8-a470-c55fb4c2f8c4">OPC_RELATIONSHIP_SELECTOR</a>  Value</th>
<th>Relationship Property</th>
<th>Description</th>
</tr>
<tr>
<td><b>OPC_RELATIONSHIP_SELECT_BY_TYPE</b></td>
<td>Relationship type</td>
<td>
Selects relationships that have a relationship type that matches <i>selectionCriterion</i> string.

</td>
</tr>
<tr>
<td><b>OPC_RELATIONSHIP_SELECT_BY_ID</b></td>
<td>Relationship identifier</td>
<td>
Selects relationships that have a relationship identifier that matches <i>selectionCriterion</i> string.

</td>
</tr>
</table>
 



When a signature is generated, the relationship selection information provided by the interface is serialized in the XML markup of the signature (signature markup). In signature markup, this information is represented by the  <b>RelationshipReference</b> and <b>RelationshipGroupReference</b> elements, which are specified in section 12. Digital Signatures in the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>. The following table shows how the elements map to relationship properties and to <a href="https://msdn.microsoft.com/5532aab1-850e-4de8-a470-c55fb4c2f8c4">OPC_RELATIONSHIP_SELECTOR</a> values.<table>
<tr>
<th>Package signature element</th>
<th>Relationship Property</th>
<th>
<a href="https://msdn.microsoft.com/5532aab1-850e-4de8-a470-c55fb4c2f8c4">OPC_RELATIONSHIP_SELECTOR</a>  Value</th>
</tr>
<tr>
<td><b>RelationshipGroupReference</b></td>
<td>Relationship type</td>
<td><b>OPC_RELATIONSHIP_SELECT_BY_TYPE</b></td>
</tr>
<tr>
<td><b>RelationshipReference</b></td>
<td>Relationship identifier</td>
<td><b>OPC_RELATIONSHIP_SELECT_BY_ID</b></td>
</tr>
</table>
 




#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">ECMA-376 OpenXML standard</a>



<b>External Resources</b>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/eb3619bb-470f-41bd-a231-d63df70592c2">IOpcRelationship</a>



<a href="https://msdn.microsoft.com/9c0bbc0d-d950-4929-9100-41a7f016a208">IOpcRelationshipSelectorEnumerator</a>



<a href="https://msdn.microsoft.com/cb23cbe2-764c-47e4-bd32-2791ddde9eee">IOpcRelationshipSelectorSet</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

