---
UID: NN:msopc.IOpcCertificateSet
title: IOpcCertificateSet (msopc.h)
description: An unordered set of certificates to be used with a signature.
helpviewer_keywords: ["IOpcCertificateSet","IOpcCertificateSet interface [Open Packaging Conventions]","IOpcCertificateSet interface [Open Packaging Conventions]","described","msopc/IOpcCertificateSet","opc.iopccertificateset"]
old-location: opc\iopccertificateset.htm
tech.root: OPC
ms.assetid: 0ac56b41-a120-4a9b-9bfa-afba1ba0f3b4
ms.date: 12/05/2018
ms.keywords: IOpcCertificateSet, IOpcCertificateSet interface [Open Packaging Conventions], IOpcCertificateSet interface [Open Packaging Conventions],described, msopc/IOpcCertificateSet, opc.iopccertificateset
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msopc.idl
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
 - IOpcCertificateSet
 - msopc/IOpcCertificateSet
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
 - IOpcCertificateSet
---

# IOpcCertificateSet interface


## -description

An unordered set of certificates to be used with a signature.

## -inheritance

The <b>IOpcCertificateSet</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcCertificateSet</b> also has these types of members:

## -remarks

Do not add the certificate that will be passed to the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignaturemanager-sign">IOpcDigitalSignature::Sign</a> method (the signer certificate) to this certificate set.

Certificates that are in a certificate chain are added to the package by calling the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopccertificateset-add">Add</a> method.

To access an <b>IOpcCertificateSet</b> interface pointer, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-getcertificateset">IOpcSigningOptions::GetCertificateSet</a> method.

When a signature is generated, certificates that were added to the package by calling <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopccertificateset-add">Add</a> are associated  with the signature.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>



<a href="/windows/desktop/SecCrypto/certificates">Certificates</a>



<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateenumerator">IOpcCertificateEnumerator</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
