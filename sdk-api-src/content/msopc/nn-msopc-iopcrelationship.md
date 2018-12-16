---
UID: NN:msopc.IOpcRelationship
title: IOpcRelationship
author: windows-sdk-content
description: Represents a relationship, which is a link between a source, which is a part or the package, and a target.
old-location: opc\iopcrelationship.htm
tech.root: OPC
ms.assetid: eb3619bb-470f-41bd-a231-d63df70592c2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IOpcRelationship, IOpcRelationship interface [Open Packaging Conventions], IOpcRelationship interface [Open Packaging Conventions],described, msopc/IOpcRelationship, opc.iopcrelationship
ms.topic: interface
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msopc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msopc.h
api_name:
 - IOpcRelationship
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcRelationship interface


## -description


Represents a relationship, which is a link between a source, which is a part or the package,  and a target.  The relationship's  target can be a part or external resource.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcRelationship</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpcRelationship</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcRelationship</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8646d592-d568-4b82-80f3-2673cd0d2721">GetId</a>
</td>
<td align="left" width="63%">
Gets the unique identifier of the relationship.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da832c8e-99e1-452a-90eb-97580f00f003">GetRelationshipType</a>
</td>
<td align="left" width="63%">
Gets the relationship type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e2587af-fce0-437a-9608-6824e861d699">GetSourceUri</a>
</td>
<td align="left" width="63%">
Gets the URI of the relationship source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5fb103c9-cb73-46b3-9102-6811d6673faf">GetTargetMode</a>
</td>
<td align="left" width="63%">
Gets a value that describes whether the relationship's target is internal  or external to the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65b04931-dc4e-4eb5-b542-a7b46c3164de">GetTargetUri</a>
</td>
<td align="left" width="63%">
Gets the URI of the relationship target.

</td>
</tr>
</table> 


## -remarks



To create a relationship object to represent a relationship, call the <a href="https://msdn.microsoft.com/0cbf7446-d94e-447f-a82b-3d56a8036c19">IOpcRelationshipSet::CreateRelationship</a> method. To get a pointer to the interface of a relationship object that represents an existing relationship, call the <a href="https://msdn.microsoft.com/f44eeae6-592e-479e-98b7-f73075906a7a">IOpcRelationshipSet::GetRelationship</a> or <a href="https://msdn.microsoft.com/6ddd7a5f-659d-45e1-aff8-dee799efd8ac">IOpcRelationshipEnumerator::GetCurrent</a> method.

Example relationship markup for a relationship that targets a part:

<div class="code"><span codelanguage="XML"><table>
<tr>
<th>XML</th>
</tr>
<tr>
<td>
<pre>&lt;Relationship Id="rId1"
    Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument"
    Target="word/document.xml" /&gt;</pre>
</td>
</tr>
</table></span></div>
Using the relationship type (<b>Type</b> attribute of the <b>Relationship</b> element)  is the definitive way  find a 
part in a package. For more information about  why the relationship type is used, see the <a href="https://msdn.microsoft.com/95da581d-3d30-4cd7-bd20-f44bf505ac0a">Parts Overview</a>.  For an example of to use the relationship type to find a part, see <a href="https://msdn.microsoft.com/d485d085-b605-41d4-a094-bd1be37d6693">Finding the Core Properties Part</a>. 

Valid identifiers for relationships conform to the restrictions for <b>xsd:ID</b>, which are documented in section 3.3.8 ID of the <a href=" http://go.microsoft.com/fwlink/p/?linkid=126664">W3C Recommendation, XML Schema Part 2: Datatypes Second Edition</a> (http://go.microsoft.com/fwlink/p/?linkid=126664).

<b>IOpcRelationship</b> interface methods provide access to relationship properties for a relationship (which is represented by a relationship object). The methods, associated properties and descriptions are listed in the following table.

<table>
<tr>
<th>Method</th>
<th>Property</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/8646d592-d568-4b82-80f3-2673cd0d2721">GetId</a>
</td>
<td>Relationship identifier</td>
<td>
The unique, arbitrary identifier of a relationship that is local to the package.

</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/da832c8e-99e1-452a-90eb-97580f00f003">GetRelationshipType</a>
</td>
<td>Relationship type</td>
<td>
The qualified name of a relationship defined by the package designer.

</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/8e2587af-fce0-437a-9608-6824e861d699">GetSourceUri</a>
</td>
<td>Source URI</td>
<td>
The URI of the relationship's source. The source URI can be the URI of the package or of a part.

</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/5fb103c9-cb73-46b3-9102-6811d6673faf">GetTargetMode</a>
</td>
<td>Target mode</td>
<td>
Indicates whether the relationship's target is internal or external to the package.

</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/65b04931-dc4e-4eb5-b542-a7b46c3164de">GetTargetUri</a>
</td>
<td>Target URI</td>
<td>
The URI of the relationship's target.

</td>
</tr>
</table>
 

For more information about relationships, see the <a href="https://msdn.microsoft.com/115430f2-8e1f-46ba-ae6e-b7f3689048ff">Open Packaging Conventions Fundamentals</a> and the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="https://msdn.microsoft.com/d485d085-b605-41d4-a094-bd1be37d6693">Finding the Core Properties Part</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/6259906d-820d-4b6e-bbeb-d9d044f2b35a">IOpcRelationshipSet</a>



<a href="https://msdn.microsoft.com/af052aa3-db7a-47de-938c-32895b8735e9">OPC_URI_TARGET_MODE</a>



<a href="https://msdn.microsoft.com/115430f2-8e1f-46ba-ae6e-b7f3689048ff">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8e071847-7eb2-4528-8402-4aaa1f5cd216">Relationships Overview</a>
 

 

