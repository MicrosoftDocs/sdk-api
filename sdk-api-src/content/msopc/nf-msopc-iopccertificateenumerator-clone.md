---
UID: NF:msopc.IOpcCertificateEnumerator.Clone
title: IOpcCertificateEnumerator::Clone (msopc.h)
description: Creates a copy of the current IOpcCertificateEnumerator interface pointer and all its descendants.
helpviewer_keywords: ["Clone","Clone method [Open Packaging Conventions]","Clone method [Open Packaging Conventions]","IOpcCertificateEnumerator interface","IOpcCertificateEnumerator interface [Open Packaging Conventions]","Clone method","IOpcCertificateEnumerator.Clone","IOpcCertificateEnumerator::Clone","msopc/IOpcCertificateEnumerator::Clone","opc.iopccertificateenumerator_clone"]
old-location: opc\iopccertificateenumerator_clone.htm
tech.root: OPC
ms.assetid: 4cf4bed8-4a6f-48f4-b72f-a13efc127b2a
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Open Packaging Conventions], Clone method [Open Packaging Conventions],IOpcCertificateEnumerator interface, IOpcCertificateEnumerator interface [Open Packaging Conventions],Clone method, IOpcCertificateEnumerator.Clone, IOpcCertificateEnumerator::Clone, msopc/IOpcCertificateEnumerator::Clone, opc.iopccertificateenumerator_clone
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
 - IOpcCertificateEnumerator::Clone
 - msopc/IOpcCertificateEnumerator::Clone
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
 - IOpcCertificateEnumerator.Clone
---

# IOpcCertificateEnumerator::Clone


## -description

Creates a copy of the current <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateenumerator">IOpcCertificateEnumerator</a> interface pointer and all its descendants.

## -parameters

### -param copy [out, retval]

A pointer to a copy of the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateenumerator">IOpcCertificateEnumerator</a> interface pointer.

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

<a href="/windows/desktop/SecCrypto/certificates">Certificates</a>



<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateenumerator">IOpcCertificateEnumerator</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateset">IOpcCertificateSet</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>