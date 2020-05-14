---
UID: NN:msopc.IOpcRelationship
title: IOpcRelationship (msopc.h)
description: Represents a relationship, which is a link between a source, which is a part or the package, and a target.
helpviewer_keywords: ["IOpcRelationship","IOpcRelationship interface [Open Packaging Conventions]","IOpcRelationship interface [Open Packaging Conventions]","described","msopc/IOpcRelationship","opc.iopcrelationship"]
old-location: opc\iopcrelationship.htm
tech.root: OPC
ms.assetid: eb3619bb-470f-41bd-a231-d63df70592c2
ms.date: 12/05/2018
ms.keywords: IOpcRelationship, IOpcRelationship interface [Open Packaging Conventions], IOpcRelationship interface [Open Packaging Conventions],described, msopc/IOpcRelationship, opc.iopcrelationship
f1_keywords:
- msopc/IOpcRelationship
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOpcRelationship interface


## -description


Represents a relationship, which is a link between a source, which is a part or the package,  and a target.  The relationship's  target can be a part or external resource.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcRelationship</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcRelationship</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationship-getid">GetId</a>
</td>
<td align="left" width="63%">
Gets the unique identifier of the relationship.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationship-getrelationshiptype">GetRelationshipType</a>
</td>
<td align="left" width="63%">
Gets the relationship type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationship-getsourceuri">GetSourceUri</a>
</td>
<td align="left" width="63%">
Gets the URI of the relationship source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationship-gettargetmode">GetTargetMode</a>
</td>
<td align="left" width="63%">
Gets a value that describes whether the relationship's target is internal  or external to the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationship-gettargeturi">GetTargetUri</a>
</td>
<td align="left" width="63%">
Gets the URI of the relationship target.

</td>
</tr>
</table> 


## -remarks



To create a relationship object to represent a relationship, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipset-createrelationship">IOpcRelationshipSet::CreateRelationship</a> method. To get a pointer to the interface of a relationship object that represents an existing relationship, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipset-getrelationship">IOpcRelationshipSet::GetRelationship</a> or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipenumerator-getcurrent">IOpcRelationshipEnumerator::GetCurrent</a> method.

Example relationship markup for a relationship that targets a part:


```xml
<Relationship Id="rId1"
    Type="http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument"
    Target="word/document.xml" />
```


Using the relationship type (<b>Type</b> attribute of the <b>Relationship</b> element)  is the definitive way  find a 
part in a package. For more information about  why the relationship type is used, see the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/parts-overview">Parts Overview</a>.  For an example of to use the relationship type to find a part, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/finding-the-core-properties-part">Finding the Core Properties Part</a>. 

Valid identifiers for relationships conform to the restrictions for <b>xsd:ID</b>, which are documented in section 3.3.8 ID of the <a href="https://www.w3.org/TR/xmlschema-2/#ID">W3C Recommendation, XML Schema Part 2: Datatypes Second Edition</a> (http://www.w3.org/TR/xmlschema-2/#ID).

<b>IOpcRelationship</b> interface methods provide access to relationship properties for a relationship (which is represented by a relationship object). The methods, associated properties and descriptions are listed in the following table.

<table>
<tr>
<th>Method</th>
<th>Property</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationship-getid">GetId</a>
</td>
<td>Relationship identifier</td>
<td>
The unique, arbitrary identifier of a relationship that is local to the package.

</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationship-getrelationshiptype">GetRelationshipType</a>
</td>
<td>Relationship type</td>
<td>
The qualified name of a relationship defined by the package designer.

</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationship-getsourceuri">GetSourceUri</a>
</td>
<td>Source URI</td>
<td>
The URI of the relationship's source. The source URI can be the URI of the package or of a part.

</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationship-gettargetmode">GetTargetMode</a>
</td>
<td>Target mode</td>
<td>
Indicates whether the relationship's target is internal or external to the package.

</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationship-gettargeturi">GetTargetUri</a>
</td>
<td>Target URI</td>
<td>
The URI of the relationship's target.

</td>
</tr>
</table>
 

For more information about relationships, see the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a> and the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="https://www.ecma-international.org/publications/standards/Ecma-376.htm">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/finding-the-core-properties-part">Finding the Core Properties Part</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipset">IOpcRelationshipSet</a>



<a href="/windows/win32/api/msopc/ne-msopc-opc_uri_target_mode">OPC_URI_TARGET_MODE</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/relationships-overview">Relationships Overview</a>
 

 

