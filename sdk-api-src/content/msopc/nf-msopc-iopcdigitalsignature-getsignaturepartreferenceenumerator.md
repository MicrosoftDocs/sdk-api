---
UID: NF:msopc.IOpcDigitalSignature.GetSignaturePartReferenceEnumerator
title: IOpcDigitalSignature::GetSignaturePartReferenceEnumerator (msopc.h)
description: Gets an enumerator of IOpcSignaturePartReference interface pointers, which represent references to parts that have been signed.
helpviewer_keywords: ["GetSignaturePartReferenceEnumerator","GetSignaturePartReferenceEnumerator method [Open Packaging Conventions]","GetSignaturePartReferenceEnumerator method [Open Packaging Conventions]","IOpcDigitalSignature interface","IOpcDigitalSignature interface [Open Packaging Conventions]","GetSignaturePartReferenceEnumerator method","IOpcDigitalSignature.GetSignaturePartReferenceEnumerator","IOpcDigitalSignature::GetSignaturePartReferenceEnumerator","msopc/IOpcDigitalSignature::GetSignaturePartReferenceEnumerator","opc.iopcdigitalsignature_getsignaturepartreferenceenumerator"]
old-location: opc\iopcdigitalsignature_getsignaturepartreferenceenumerator.htm
tech.root: OPC
ms.assetid: d8d1507e-b72f-4eb7-bd3d-4f4a26516c18
ms.date: 12/05/2018
ms.keywords: GetSignaturePartReferenceEnumerator, GetSignaturePartReferenceEnumerator method [Open Packaging Conventions], GetSignaturePartReferenceEnumerator method [Open Packaging Conventions],IOpcDigitalSignature interface, IOpcDigitalSignature interface [Open Packaging Conventions],GetSignaturePartReferenceEnumerator method, IOpcDigitalSignature.GetSignaturePartReferenceEnumerator, IOpcDigitalSignature::GetSignaturePartReferenceEnumerator, msopc/IOpcDigitalSignature::GetSignaturePartReferenceEnumerator, opc.iopcdigitalsignature_getsignaturepartreferenceenumerator
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
 - IOpcDigitalSignature::GetSignaturePartReferenceEnumerator
 - msopc/IOpcDigitalSignature::GetSignaturePartReferenceEnumerator
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
 - IOpcDigitalSignature.GetSignaturePartReferenceEnumerator
---

# IOpcDigitalSignature::GetSignaturePartReferenceEnumerator


## -description

Gets an enumerator of <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturepartreference">IOpcSignaturePartReference</a> interface pointers, which represent references to parts that have been signed.

## -parameters

### -param partReferenceEnumerator [out, retval]

A pointer to an enumerator of <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturepartreference">IOpcSignaturePartReference</a> interface pointers, which represent references to parts that have been signed.

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
The <i>partReferenceEnumerator</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturepartreferenceenumerator">IOpcSignaturePartReferenceEnumerator</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturepartreferenceset">IOpcSignaturePartReferenceSet</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>