---
UID: NF:msopc.IOpcSignatureRelationshipReference.GetRelationshipSelectorEnumerator
title: IOpcSignatureRelationshipReference::GetRelationshipSelectorEnumerator (msopc.h)
description: Gets an enumerator of IOpcRelationshipSelector interface pointers that represent the techniques used to select the subset of relationships in the referenced Relationships part.
helpviewer_keywords: ["GetRelationshipSelectorEnumerator","GetRelationshipSelectorEnumerator method [Open Packaging Conventions]","GetRelationshipSelectorEnumerator method [Open Packaging Conventions]","IOpcSignatureRelationshipReference interface","IOpcSignatureRelationshipReference interface [Open Packaging Conventions]","GetRelationshipSelectorEnumerator method","IOpcSignatureRelationshipReference.GetRelationshipSelectorEnumerator","IOpcSignatureRelationshipReference::GetRelationshipSelectorEnumerator","msopc/IOpcSignatureRelationshipReference::GetRelationshipSelectorEnumerator","opc.iopcsignaturerelationshipreference_getrelationshipselectorenumerator"]
old-location: opc\iopcsignaturerelationshipreference_getrelationshipselectorenumerator.htm
tech.root: OPC
ms.assetid: a9e1e9e8-d318-4e72-ba52-d020e58f85ff
ms.date: 12/05/2018
ms.keywords: GetRelationshipSelectorEnumerator, GetRelationshipSelectorEnumerator method [Open Packaging Conventions], GetRelationshipSelectorEnumerator method [Open Packaging Conventions],IOpcSignatureRelationshipReference interface, IOpcSignatureRelationshipReference interface [Open Packaging Conventions],GetRelationshipSelectorEnumerator method, IOpcSignatureRelationshipReference.GetRelationshipSelectorEnumerator, IOpcSignatureRelationshipReference::GetRelationshipSelectorEnumerator, msopc/IOpcSignatureRelationshipReference::GetRelationshipSelectorEnumerator, opc.iopcsignaturerelationshipreference_getrelationshipselectorenumerator
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
 - IOpcSignatureRelationshipReference::GetRelationshipSelectorEnumerator
 - msopc/IOpcSignatureRelationshipReference::GetRelationshipSelectorEnumerator
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
 - IOpcSignatureRelationshipReference.GetRelationshipSelectorEnumerator
---

# IOpcSignatureRelationshipReference::GetRelationshipSelectorEnumerator


## -description

Gets an enumerator of <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselector">IOpcRelationshipSelector</a> interface pointers that represent the techniques used to select the subset of relationships in the referenced Relationships part.

## -parameters

### -param selectorEnumerator [out, retval]

A pointer to an enumerator of <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselector">IOpcRelationshipSelector</a> interface pointers.

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
The <i>selectorEnumerator</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreferenceenumerator">IOpcSignatureRelationshipReferenceEnumerator</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>