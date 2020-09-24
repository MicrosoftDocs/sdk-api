---
UID: NF:msopc.IOpcSignatureReferenceEnumerator.Clone
title: IOpcSignatureReferenceEnumerator::Clone (msopc.h)
description: Creates a copy of the current IOpcSignatureReferenceEnumerator interface pointer and all its descendants.
helpviewer_keywords: ["Clone","Clone method [Open Packaging Conventions]","Clone method [Open Packaging Conventions]","IOpcSignatureReferenceEnumerator interface","IOpcSignatureReferenceEnumerator interface [Open Packaging Conventions]","Clone method","IOpcSignatureReferenceEnumerator.Clone","IOpcSignatureReferenceEnumerator::Clone","msopc/IOpcSignatureReferenceEnumerator::Clone","opc.iopcsignaturereferenceenumerator_clone"]
old-location: opc\iopcsignaturereferenceenumerator_clone.htm
tech.root: OPC
ms.assetid: a0a2d699-ea48-40f9-bb27-5008012f9c9c
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Open Packaging Conventions], Clone method [Open Packaging Conventions],IOpcSignatureReferenceEnumerator interface, IOpcSignatureReferenceEnumerator interface [Open Packaging Conventions],Clone method, IOpcSignatureReferenceEnumerator.Clone, IOpcSignatureReferenceEnumerator::Clone, msopc/IOpcSignatureReferenceEnumerator::Clone, opc.iopcsignaturereferenceenumerator_clone
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
 - IOpcSignatureReferenceEnumerator::Clone
 - msopc/IOpcSignatureReferenceEnumerator::Clone
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
 - IOpcSignatureReferenceEnumerator.Clone
---

# IOpcSignatureReferenceEnumerator::Clone


## -description

Creates a copy of the current <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceenumerator">IOpcSignatureReferenceEnumerator</a> interface pointer and all its descendants.

## -parameters

### -param copy [out, retval]

A pointer to a copy of the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceenumerator">IOpcSignatureReferenceEnumerator</a> interface pointer.

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
The <i>copy</i> parameter is <b>NULL</b>.

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
</table>

## -remarks

The copy has a current position  and set that are identical to the current enumerator.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceenumerator">IOpcSignatureReferenceEnumerator</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>