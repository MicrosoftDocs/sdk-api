---
UID: NF:msopc.IOpcSignatureReferenceEnumerator.MovePrevious
title: IOpcSignatureReferenceEnumerator::MovePrevious (msopc.h)
description: Moves the current position of the enumerator to the previous IOpcSignatureReferenceinterface pointer.
helpviewer_keywords: ["IOpcSignatureReferenceEnumerator interface [Open Packaging Conventions]","MovePrevious method","IOpcSignatureReferenceEnumerator.MovePrevious","IOpcSignatureReferenceEnumerator::MovePrevious","MovePrevious","MovePrevious method [Open Packaging Conventions]","MovePrevious method [Open Packaging Conventions]","IOpcSignatureReferenceEnumerator interface","msopc/IOpcSignatureReferenceEnumerator::MovePrevious","opc.iopcsignaturereferenceenumerator_moveprevious"]
old-location: opc\iopcsignaturereferenceenumerator_moveprevious.htm
tech.root: OPC
ms.assetid: 7ff697a4-45fe-46cd-8d36-96bafcb32aa1
ms.date: 12/05/2018
ms.keywords: IOpcSignatureReferenceEnumerator interface [Open Packaging Conventions],MovePrevious method, IOpcSignatureReferenceEnumerator.MovePrevious, IOpcSignatureReferenceEnumerator::MovePrevious, MovePrevious, MovePrevious method [Open Packaging Conventions], MovePrevious method [Open Packaging Conventions],IOpcSignatureReferenceEnumerator interface, msopc/IOpcSignatureReferenceEnumerator::MovePrevious, opc.iopcsignaturereferenceenumerator_moveprevious
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
 - IOpcSignatureReferenceEnumerator::MovePrevious
 - msopc/IOpcSignatureReferenceEnumerator::MovePrevious
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
 - IOpcSignatureReferenceEnumerator.MovePrevious
---

# IOpcSignatureReferenceEnumerator::MovePrevious


## -description

Moves the current position of the enumerator to the previous <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereference">IOpcSignatureReference</a> interface pointer.

## -parameters

### -param hasPrevious [out, retval]

A Boolean value that indicates the status of the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereference">IOpcSignatureReference</a> interface pointer at the current position.

The value of <i>hasPrevious</i> is only valid when the method succeeds.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>TRUE</dt>
</dl>
</td>
<td width="60%">
The current position of the enumerator has been moved to the previous pointer in the collection, and that pointer is valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>FALSE</dt>
</dl>
</td>
<td width="60%">
The current position of the enumerator has been moved past the beginning of the collection and is no longer valid.

</td>
</tr>
</table>

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
The <i>hasPrevious</i> parameter is <b>NULL</b>.

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
<dt><b>OPC_E_ENUM_CANNOT_MOVE_PREVIOUS</b></dt>
<dt>0x80510052</dt>
</dl>
</td>
<td width="60%">
The current position already precedes the first item of the enumerator.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceenumerator">IOpcSignatureReferenceEnumerator</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceset">IOpcSignatureReferenceSet</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>