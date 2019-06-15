---
UID: NN:msopc.IOpcRelationshipSet
title: IOpcRelationshipSet (msopc.h)
author: windows-sdk-content
description: Represents a Relationships part as an unordered set of IOpcRelationship interface pointers to relationship objects.
old-location: opc\iopcrelationshipset.htm
tech.root: OPC
ms.assetid: 6259906d-820d-4b6e-bbeb-d9d044f2b35a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOpcRelationshipSet, IOpcRelationshipSet interface [Open Packaging Conventions], IOpcRelationshipSet interface [Open Packaging Conventions],described, msopc/IOpcRelationshipSet, opc.iopcrelationshipset
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
ms.custom: 19H1
---

# IOpcRelationshipSet interface


## -description


Represents a Relationships part as an unordered set of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface pointers to relationship objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcRelationshipSet</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcRelationshipSet</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipset-createrelationship">CreateRelationship</a>
</td>
<td align="left" width="63%">
              Creates a relationship object that represents a specified relationship, then adds to  the set a pointer to the object's <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipset-deleterelationship">DeleteRelationship</a>
</td>
<td align="left" width="63%">
Deletes a specified <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface pointer from the set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipset-getenumerator">GetEnumerator</a>
</td>
<td align="left" width="63%">
Gets an enumerator of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface pointers in the set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipset-getenumeratorfortype">GetEnumeratorForType</a>
</td>
<td align="left" width="63%">
Gets an enumerator of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface pointers in the set that point to representations of relationships  that have a specified relationship type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipset-getrelationship">GetRelationship</a>
</td>
<td align="left" width="63%">
Gets a relationship object from the set that represents a specified relationship.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipset-getrelationshipscontentstream">GetRelationshipsContentStream</a>
</td>
<td align="left" width="63%">
            Gets a read-only stream that contains the part content of the Relationships part represented by the set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipset-relationshipexists">RelationshipExists</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether a specified relationship  is represented as a relationship object in the set.

</td>
</tr>
</table> 


## -remarks



When a relationship object is created and a pointer to it is added to the set, the relationship it represents is saved when the package is saved.

When an  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface pointer is deleted from the set, the relationship it represents is not saved when the package is saved.

If a relationship is represented in the set, the relationship is stored in the Relationships part represented as the set.

For how to form the part name for the target of a relationship, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/resolving-a-part-name-from-a-relationship-s-target-uri">Resolving a Part Name from a Target URI</a>.

For more information about relationships, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a> and the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>.

The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface provides access to relationship properties. For details about these properties, see the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/relationships-overview">Relationships Overview</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipenumerator">IOpcRelationshipEnumerator</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/relationships-overview">Relationships Overview</a>
 

 

