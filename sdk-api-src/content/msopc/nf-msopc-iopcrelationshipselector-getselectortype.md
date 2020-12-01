---
UID: NF:msopc.IOpcRelationshipSelector.GetSelectorType
title: IOpcRelationshipSelector::GetSelectorType (msopc.h)
description: Gets a value that describes how relationships are selected to be referenced for signing.
helpviewer_keywords: ["GetSelectorType","GetSelectorType method [Open Packaging Conventions]","GetSelectorType method [Open Packaging Conventions]","IOpcRelationshipSelector interface","IOpcRelationshipSelector interface [Open Packaging Conventions]","GetSelectorType method","IOpcRelationshipSelector.GetSelectorType","IOpcRelationshipSelector::GetSelectorType","msopc/IOpcRelationshipSelector::GetSelectorType","opc.iopcrelationshipselector_getselectortype"]
old-location: opc\iopcrelationshipselector_getselectortype.htm
tech.root: OPC
ms.assetid: 583f56e5-c374-4f79-badd-35eb5eecef70
ms.date: 12/05/2018
ms.keywords: GetSelectorType, GetSelectorType method [Open Packaging Conventions], GetSelectorType method [Open Packaging Conventions],IOpcRelationshipSelector interface, IOpcRelationshipSelector interface [Open Packaging Conventions],GetSelectorType method, IOpcRelationshipSelector.GetSelectorType, IOpcRelationshipSelector::GetSelectorType, msopc/IOpcRelationshipSelector::GetSelectorType, opc.iopcrelationshipselector_getselectortype
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OpcDigitalSignature.idl
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
 - IOpcRelationshipSelector::GetSelectorType
 - msopc/IOpcRelationshipSelector::GetSelectorType
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
 - IOpcRelationshipSelector.GetSelectorType
---

# IOpcRelationshipSelector::GetSelectorType


## -description

Gets a value that describes how relationships are selected to be referenced for signing.

## -parameters

### -param selector [out, retval]

A value that describes which <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface property will be compared to the string returned by the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipselector-getselectioncriterion">GetSelectionCriterion</a> method.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>selector</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

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
 




#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselector">IOpcRelationshipSelector</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselectorenumerator">IOpcRelationshipSelectorEnumerator</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselectorset">IOpcRelationshipSelectorSet</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>