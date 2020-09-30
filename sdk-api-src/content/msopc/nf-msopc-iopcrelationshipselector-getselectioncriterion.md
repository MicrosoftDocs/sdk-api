---
UID: NF:msopc.IOpcRelationshipSelector.GetSelectionCriterion
title: IOpcRelationshipSelector::GetSelectionCriterion (msopc.h)
description: Gets a string that is used to select relationships to be referenced for signing.
helpviewer_keywords: ["GetSelectionCriterion","GetSelectionCriterion method [Open Packaging Conventions]","GetSelectionCriterion method [Open Packaging Conventions]","IOpcRelationshipSelector interface","IOpcRelationshipSelector interface [Open Packaging Conventions]","GetSelectionCriterion method","IOpcRelationshipSelector.GetSelectionCriterion","IOpcRelationshipSelector::GetSelectionCriterion","msopc/IOpcRelationshipSelector::GetSelectionCriterion","opc.iopcrelationshipselector_getselectioncriterion"]
old-location: opc\iopcrelationshipselector_getselectioncriterion.htm
tech.root: OPC
ms.assetid: ac1f0347-9b89-4d8f-b0cb-14708e7a6e55
ms.date: 12/05/2018
ms.keywords: GetSelectionCriterion, GetSelectionCriterion method [Open Packaging Conventions], GetSelectionCriterion method [Open Packaging Conventions],IOpcRelationshipSelector interface, IOpcRelationshipSelector interface [Open Packaging Conventions],GetSelectionCriterion method, IOpcRelationshipSelector.GetSelectionCriterion, IOpcRelationshipSelector::GetSelectionCriterion, msopc/IOpcRelationshipSelector::GetSelectionCriterion, opc.iopcrelationshipselector_getselectioncriterion
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
 - IOpcRelationshipSelector::GetSelectionCriterion
 - msopc/IOpcRelationshipSelector::GetSelectionCriterion
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
 - IOpcRelationshipSelector.GetSelectionCriterion
---

# IOpcRelationshipSelector::GetSelectionCriterion


## -description

Gets a string that is used to select relationships to be referenced for signing.

## -parameters

### -param selectionCriterion [out, retval]

A string used to select relationships  to be referenced for signing.

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
The <i>selectionCriterion</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method allocates memory used by the string returned in <i>selectionCriterion</i>.  If the method succeeds, call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free the memory.

Use the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselector">IOpcRelationshipSelector</a> interface methods to select relationships for signing. A relationship is selected if its type or identifier matches the string that is retrieved by calling the <b>GetSelectionCriterion</b> method. This string is either a relationship type or a relationship identifier.  Call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipselector-getselectortype">GetSelectorType</a> method to get an <a href="/windows/win32/api/msopc/ne-msopc-opc_relationship_selector">OPC_RELATIONSHIP_SELECTOR</a> value to determine whether the string is a relationship type or an identifier. To access these relationship properties, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationship-getrelationshiptype">IOpcRelationship::GetRelationshipType</a> and <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationship-getid">IOpcRelationship::GetId</a> methods.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselector">IOpcRelationshipSelector</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselectorenumerator">IOpcRelationshipSelectorEnumerator</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselectorset">IOpcRelationshipSelectorSet</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>