---
UID: NF:msopc.IOpcSignatureRelationshipReferenceEnumerator.GetCurrent
title: IOpcSignatureRelationshipReferenceEnumerator::GetCurrent (msopc.h)
description: Gets the IOpcSignatureRelationshipReference interface pointer at the current position of the enumerator.
helpviewer_keywords: ["GetCurrent","GetCurrent method [Open Packaging Conventions]","GetCurrent method [Open Packaging Conventions]","IOpcSignatureRelationshipReferenceEnumerator interface","IOpcSignatureRelationshipReferenceEnumerator interface [Open Packaging Conventions]","GetCurrent method","IOpcSignatureRelationshipReferenceEnumerator.GetCurrent","IOpcSignatureRelationshipReferenceEnumerator::GetCurrent","msopc/IOpcSignatureRelationshipReferenceEnumerator::GetCurrent","opc.iopcsignaturerelationshipreferenceenumerator_getcurrent"]
old-location: opc\iopcsignaturerelationshipreferenceenumerator_getcurrent.htm
tech.root: OPC
ms.assetid: 18aac7c9-db1a-4fc5-896e-7a02c12788f2
ms.date: 12/05/2018
ms.keywords: GetCurrent, GetCurrent method [Open Packaging Conventions], GetCurrent method [Open Packaging Conventions],IOpcSignatureRelationshipReferenceEnumerator interface, IOpcSignatureRelationshipReferenceEnumerator interface [Open Packaging Conventions],GetCurrent method, IOpcSignatureRelationshipReferenceEnumerator.GetCurrent, IOpcSignatureRelationshipReferenceEnumerator::GetCurrent, msopc/IOpcSignatureRelationshipReferenceEnumerator::GetCurrent, opc.iopcsignaturerelationshipreferenceenumerator_getcurrent
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
 - IOpcSignatureRelationshipReferenceEnumerator::GetCurrent
 - msopc/IOpcSignatureRelationshipReferenceEnumerator::GetCurrent
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
 - IOpcSignatureRelationshipReferenceEnumerator.GetCurrent
---

# IOpcSignatureRelationshipReferenceEnumerator::GetCurrent


## -description

Gets the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a> interface pointer at the current position of the enumerator.

## -parameters

### -param relationshipReference [out, retval]

An <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a> interface pointer.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code/value</th>
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
The <i>partReference</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_ENUM_COLLECTION_CHANGED</b></dt>
<dt>0x80510050</dt>
</dl>
</td>
<td width="60%">
The enumerator is invalid because the underlying set has changed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_ENUM_INVALID_POSITION</b></dt>
<dt>0x80510053</dt>
</dl>
</td>
<td width="60%">
The enumerator cannot perform this operation from its current position.

</td>
</tr>
</table>

## -remarks

When an enumerator is created, the current position precedes the first pointer. To set the current position to the first pointer of the enumerator, call the  <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreferenceenumerator-movenext">MoveNext</a> method after creating the enumerator.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreferenceenumerator">IOpcSignatureRelationshipReferenceEnumerator</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>