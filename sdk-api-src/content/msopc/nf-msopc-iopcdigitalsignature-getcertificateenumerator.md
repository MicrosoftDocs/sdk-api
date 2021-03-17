---
UID: NF:msopc.IOpcDigitalSignature.GetCertificateEnumerator
title: IOpcDigitalSignature::GetCertificateEnumerator (msopc.h)
description: Gets an enumerator of certificates that are used in the signature.
helpviewer_keywords: ["GetCertificateEnumerator","GetCertificateEnumerator method [Open Packaging Conventions]","GetCertificateEnumerator method [Open Packaging Conventions]","IOpcDigitalSignature interface","IOpcDigitalSignature interface [Open Packaging Conventions]","GetCertificateEnumerator method","IOpcDigitalSignature.GetCertificateEnumerator","IOpcDigitalSignature::GetCertificateEnumerator","msopc/IOpcDigitalSignature::GetCertificateEnumerator","opc.iopcdigitalsignature_getcertificateenumerator"]
old-location: opc\iopcdigitalsignature_getcertificateenumerator.htm
tech.root: OPC
ms.assetid: 5b5b803f-fc61-41fa-aa73-eefb1c1d2f00
ms.date: 12/05/2018
ms.keywords: GetCertificateEnumerator, GetCertificateEnumerator method [Open Packaging Conventions], GetCertificateEnumerator method [Open Packaging Conventions],IOpcDigitalSignature interface, IOpcDigitalSignature interface [Open Packaging Conventions],GetCertificateEnumerator method, IOpcDigitalSignature.GetCertificateEnumerator, IOpcDigitalSignature::GetCertificateEnumerator, msopc/IOpcDigitalSignature::GetCertificateEnumerator, opc.iopcdigitalsignature_getcertificateenumerator
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
 - IOpcDigitalSignature::GetCertificateEnumerator
 - msopc/IOpcDigitalSignature::GetCertificateEnumerator
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
 - IOpcDigitalSignature.GetCertificateEnumerator
---

# IOpcDigitalSignature::GetCertificateEnumerator


## -description

Gets an enumerator of certificates that are used in the signature.

## -parameters

### -param certificateEnumerator [out, retval]

A pointer to an enumerator of pointers to <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structures that are used in the signature.

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
The <i>certificateEnumerator</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/windows/desktop/SecCrypto/digital-certificates">Digital Certificates</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateenumerator">IOpcCertificateEnumerator</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateset">IOpcCertificateSet</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>