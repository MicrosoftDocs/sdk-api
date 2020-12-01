---
UID: NF:msopc.IOpcCertificateSet.Add
title: IOpcCertificateSet::Add (msopc.h)
description: Adds a certificate to the set.
helpviewer_keywords: ["Add","Add method [Open Packaging Conventions]","Add method [Open Packaging Conventions]","IOpcCertificateSet interface","IOpcCertificateSet interface [Open Packaging Conventions]","Add method","IOpcCertificateSet.Add","IOpcCertificateSet::Add","msopc/IOpcCertificateSet::Add","opc.iopccertificateset_add"]
old-location: opc\iopccertificateset_add.htm
tech.root: OPC
ms.assetid: d14e9a1e-dda3-4b57-9882-0fd473a19e8c
ms.date: 12/05/2018
ms.keywords: Add, Add method [Open Packaging Conventions], Add method [Open Packaging Conventions],IOpcCertificateSet interface, IOpcCertificateSet interface [Open Packaging Conventions],Add method, IOpcCertificateSet.Add, IOpcCertificateSet::Add, msopc/IOpcCertificateSet::Add, opc.iopccertificateset_add
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
 - IOpcCertificateSet::Add
 - msopc/IOpcCertificateSet::Add
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
 - IOpcCertificateSet.Add
---

# IOpcCertificateSet::Add


## -description

Adds a certificate to the set.

## -parameters

### -param certificate [in]

A 
       <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> 
       structure that contains the certificate to be added.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, 
       those in the following table.

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
The <i>certificate</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Certificates that are in a certificate chain are added to the package by calling the 
    <b>Add</b> method.

When a signature is 
    generated, certificates that were added to the package by calling 
    <b>Add</b> are associated  with the signature.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the 
    <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/windows/desktop/SecCrypto/certificates">Certificates</a>



<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateset">IOpcCertificateSet</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>