---
UID: NN:msopc.IOpcRelationshipSelector
title: IOpcRelationshipSelector (msopc.h)
description: Represents how to select, from a Relationships part, the relationships to be referenced for signing.
helpviewer_keywords: ["IOpcRelationshipSelector","IOpcRelationshipSelector interface [Open Packaging Conventions]","IOpcRelationshipSelector interface [Open Packaging Conventions]","described","msopc/IOpcRelationshipSelector","opc.iopcrelationshipselector"]
old-location: opc\iopcrelationshipselector.htm
tech.root: OPC
ms.assetid: 077f37c3-76af-4b96-9e3a-9fd9b865d941
ms.date: 12/05/2018
ms.keywords: IOpcRelationshipSelector, IOpcRelationshipSelector interface [Open Packaging Conventions], IOpcRelationshipSelector interface [Open Packaging Conventions],described, msopc/IOpcRelationshipSelector, opc.iopcrelationshipselector
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOpcRelationshipSelector
 - msopc/IOpcRelationshipSelector
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msopc.h
api_name:
 - IOpcRelationshipSelector
---

# IOpcRelationshipSelector interface


## -description

Represents how to select, from a Relationships part, the relationships to be referenced for signing.

## -inheritance

The <b>IOpcRelationshipSelector</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcRelationshipSelector</b> also has these types of members:

## -remarks

To create an 
				 <b>IOpcRelationshipSelector</b> interface pointer, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipselectorset-create">IOpcRelationshipSelectorSet::Create</a> method.

To access an <b>IOpcRelationshipSelector</b>, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipselectorenumerator-getcurrent">IOpcRelationshipSelectorEnumerator::GetCurrent</a> method.

Use the <b>IOpcRelationshipSelector</b> interface methods to select relationships for signing. A relationship is selected if its type or identifier matches the string that is retrieved by calling the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipselector-getselectioncriterion">GetSelectionCriterion</a> method. This string is either a relationship type or a relationship identifier.  Call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipselector-getselectortype">GetSelectorType</a> method to get an <a href="/windows/win32/api/msopc/ne-msopc-opc_relationship_selector">OPC_RELATIONSHIP_SELECTOR</a> value to determine whether the string is a relationship type or an identifier. To access these relationship properties, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationship-getrelationshiptype">IOpcRelationship::GetRelationshipType</a> and <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationship-getid">IOpcRelationship::GetId</a> methods.

The following table shows how <a href="/windows/win32/api/msopc/ne-msopc-opc_relationship_selector">OPC_RELATIONSHIP_SELECTOR</a> values map to the relationship type and relationship identifier properties.<table>
<tr>
<th>
<a href="/windows/win32/api/msopc/ne-msopc-opc_relationship_selector">OPC_RELATIONSHIP_SELECTOR</a>  Value</th>
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
 



When a signature is generated, the relationship selection information provided by the interface is serialized in the XML markup of the signature (signature markup). In signature markup, this information is represented by the  <b>RelationshipReference</b> and <b>RelationshipGroupReference</b> elements, which are specified in section 12. Digital Signatures in the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>. The following table shows how the elements map to relationship properties and to <a href="/windows/win32/api/msopc/ne-msopc-opc_relationship_selector">OPC_RELATIONSHIP_SELECTOR</a> values.<table>
<tr>
<th>Package signature element</th>
<th>Relationship Property</th>
<th>
<a href="/windows/win32/api/msopc/ne-msopc-opc_relationship_selector">OPC_RELATIONSHIP_SELECTOR</a>  Value</th>
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

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 OpenXML standard</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselectorenumerator">IOpcRelationshipSelectorEnumerator</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselectorset">IOpcRelationshipSelectorSet</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
