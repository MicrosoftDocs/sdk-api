---
UID: NN:msopc.IOpcCertificateEnumerator
title: IOpcCertificateEnumerator (msopc.h)
description: A read-only enumerator of pointers to CERT_CONTEXT structures.
helpviewer_keywords: ["IOpcCertificateEnumerator","IOpcCertificateEnumerator interface [Open Packaging Conventions]","IOpcCertificateEnumerator interface [Open Packaging Conventions]","described","msopc/IOpcCertificateEnumerator","opc.iopccertificateenumerator"]
old-location: opc\iopccertificateenumerator.htm
tech.root: OPC
ms.assetid: a66ad728-9d20-44d9-a363-1d2a7927d810
ms.date: 12/05/2018
ms.keywords: IOpcCertificateEnumerator, IOpcCertificateEnumerator interface [Open Packaging Conventions], IOpcCertificateEnumerator interface [Open Packaging Conventions],described, msopc/IOpcCertificateEnumerator, opc.iopccertificateenumerator
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
 - IOpcCertificateEnumerator
 - msopc/IOpcCertificateEnumerator
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
 - IOpcCertificateEnumerator
---

# IOpcCertificateEnumerator interface


## -description

A read-only enumerator of pointers to <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structures.

## -inheritance

The <b>IOpcCertificateEnumerator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcCertificateEnumerator</b> also has these types of members:

## -remarks

When an enumerator is created, the current position precedes the first pointer of the enumerator. To set the current position to the first pointer, call the  <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopccertificateenumerator-movenext">MoveNext</a> method after the enumerator is created.

Changes to the set will invalidate the enumerator and all subsequent calls to it will fail.

To get an <b>IOpcCertificateEnumerator</b> interface pointer, call the  <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopccertificateset-getenumerator">IOpcCertificateSet::GetEnumerator</a> or <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getcertificateenumerator">IOpcDigitalSignature::GetCertificateEnumerator</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/windows/desktop/SecCrypto/certificates">Certificates</a>



<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateset">IOpcCertificateSet</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
