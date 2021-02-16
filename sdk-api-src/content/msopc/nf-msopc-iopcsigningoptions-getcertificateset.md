---
UID: NF:msopc.IOpcSigningOptions.GetCertificateSet
title: IOpcSigningOptions::GetCertificateSet (msopc.h)
description: Gets an IOpcCertificateSet interface pointer.
helpviewer_keywords: ["GetCertificateSet","GetCertificateSet method [Open Packaging Conventions]","GetCertificateSet method [Open Packaging Conventions]","IOpcSigningOptions interface","IOpcSigningOptions interface [Open Packaging Conventions]","GetCertificateSet method","IOpcSigningOptions.GetCertificateSet","IOpcSigningOptions::GetCertificateSet","msopc/IOpcSigningOptions::GetCertificateSet","opc.iopcsigningoptions_getcertificateset"]
old-location: opc\iopcsigningoptions_getcertificateset.htm
tech.root: OPC
ms.assetid: df212397-7ec9-4a42-bebb-61799b7ca78e
ms.date: 12/05/2018
ms.keywords: GetCertificateSet, GetCertificateSet method [Open Packaging Conventions], GetCertificateSet method [Open Packaging Conventions],IOpcSigningOptions interface, IOpcSigningOptions interface [Open Packaging Conventions],GetCertificateSet method, IOpcSigningOptions.GetCertificateSet, IOpcSigningOptions::GetCertificateSet, msopc/IOpcSigningOptions::GetCertificateSet, opc.iopcsigningoptions_getcertificateset
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
 - IOpcSigningOptions::GetCertificateSet
 - msopc/IOpcSigningOptions::GetCertificateSet
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
 - IOpcSigningOptions.GetCertificateSet
---

# IOpcSigningOptions::GetCertificateSet


## -description

Gets an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateset">IOpcCertificateSet</a> interface pointer.

## -parameters

### -param certificateSet [out, retval]

An <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateset">IOpcCertificateSet</a> interface pointer.

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
The <i>certificateSet</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method gets a set that provides methods enabling the addition and removal of certificates from a certificate chain that will be associated with the signature when it is generated.

Do not include the certificate use to generate the signature in this set. This certificate, the signer certificate, is required for signature generation. To generate the signature, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignaturemanager-sign">IOpcDigitalSignatureManager::Sign</a> method with the <i>certificate</i> parameter value set to a pointer to the signer certificate.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignaturemanager">IOpcDigitalSignatureManager</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>