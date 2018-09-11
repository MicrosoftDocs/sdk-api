---
UID: NN:msopc.IOpcRelationshipSet
title: IOpcRelationshipSet
author: windows-sdk-content
description: Represents a Relationships part as an unordered set of IOpcRelationship interface pointers to relationship objects.
old-location: opc\iopcrelationshipset.htm
tech.root: OPC
ms.assetid: 6259906d-820d-4b6e-bbeb-d9d044f2b35a
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IOpcRelationshipSet, IOpcRelationshipSet interface [Open Packaging Conventions], IOpcRelationshipSet interface [Open Packaging Conventions],described, msopc/IOpcRelationshipSet, opc.iopcrelationshipset
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IOpcRelationshipSet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcRelationshipSet interface


## -description


Represents a Relationships part as an unordered set of <a href="https://msdn.microsoft.com/eb3619bb-470f-41bd-a231-d63df70592c2">IOpcRelationship</a> interface pointers to relationship objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcRelationshipSet</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpcRelationshipSet</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcRelationshipSet</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0cbf7446-d94e-447f-a82b-3d56a8036c19">CreateRelationship</a>
</td>
<td align="left" width="63%">
              Creates a relationship object that represents a specified relationship, then adds to  the set a pointer to the object's <a href="https://msdn.microsoft.com/eb3619bb-470f-41bd-a231-d63df70592c2">IOpcRelationship</a> interface.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa452e8d-10dd-4cc4-a56b-a09d841dc46a">DeleteRelationship</a>
</td>
<td align="left" width="63%">
Deletes a specified <a href="https://msdn.microsoft.com/eb3619bb-470f-41bd-a231-d63df70592c2">IOpcRelationship</a> interface pointer from the set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bcffa20d-b86e-4bfe-9f67-7404d44acb03">GetEnumerator</a>
</td>
<td align="left" width="63%">
Gets an enumerator of <a href="https://msdn.microsoft.com/eb3619bb-470f-41bd-a231-d63df70592c2">IOpcRelationship</a> interface pointers in the set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b389660-f74d-48ae-a16b-5822661f0015">GetEnumeratorForType</a>
</td>
<td align="left" width="63%">
Gets an enumerator of the <a href="https://msdn.microsoft.com/eb3619bb-470f-41bd-a231-d63df70592c2">IOpcRelationship</a> interface pointers in the set that point to representations of relationships  that have a specified relationship type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f44eeae6-592e-479e-98b7-f73075906a7a">GetRelationship</a>
</td>
<td align="left" width="63%">
Gets a relationship object from the set that represents a specified relationship.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/648e5bd1-25cc-48df-8120-ca1756eff8f7">GetRelationshipsContentStream</a>
</td>
<td align="left" width="63%">
            Gets a read-only stream that contains the part content of the Relationships part represented by the set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18c989e2-8def-492d-ac57-014f9b6fcb22">RelationshipExists</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether a specified relationship  is represented as a relationship object in the set.

</td>
</tr>
</table> 


## -remarks



When a relationship object is created and a pointer to it is added to the set, the relationship it represents is saved when the package is saved.

When an  <a href="https://msdn.microsoft.com/eb3619bb-470f-41bd-a231-d63df70592c2">IOpcRelationship</a> interface pointer is deleted from the set, the relationship it represents is not saved when the package is saved.

If a relationship is represented in the set, the relationship is stored in the Relationships part represented as the set.

For how to form the part name for the target of a relationship, see <a href="https://msdn.microsoft.com/e95db16f-ac25-4936-babb-20f2afdd2f06">Resolving a Part Name from a Target URI</a>.

For more information about relationships, see <a href="https://msdn.microsoft.com/115430f2-8e1f-46ba-ae6e-b7f3689048ff">Open Packaging Conventions Fundamentals</a> and the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>.

The <a href="https://msdn.microsoft.com/eb3619bb-470f-41bd-a231-d63df70592c2">IOpcRelationship</a> interface provides access to relationship properties. For details about these properties, see the <a href="https://msdn.microsoft.com/8e071847-7eb2-4528-8402-4aaa1f5cd216">Relationships Overview</a> and <a href="https://msdn.microsoft.com/eb3619bb-470f-41bd-a231-d63df70592c2">IOpcRelationship</a>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/8d8071cb-89ea-421e-9475-04a028317198">IOpcRelationshipEnumerator</a>



<a href="https://msdn.microsoft.com/115430f2-8e1f-46ba-ae6e-b7f3689048ff">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8e071847-7eb2-4528-8402-4aaa1f5cd216">Relationships Overview</a>
 

 

