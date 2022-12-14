---
UID: NN:msopc.IOpcSigningOptions
title: IOpcSigningOptions (msopc.h)
description: Provides methods to set and access information required to generate a signature.
helpviewer_keywords: ["IOpcSigningOptions","IOpcSigningOptions interface [Open Packaging Conventions]","IOpcSigningOptions interface [Open Packaging Conventions]","described","msopc/IOpcSigningOptions","opc.iopcsigningoptions"]
old-location: opc\iopcsigningoptions.htm
tech.root: OPC
ms.assetid: 5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec
ms.date: 12/05/2018
ms.keywords: IOpcSigningOptions, IOpcSigningOptions interface [Open Packaging Conventions], IOpcSigningOptions interface [Open Packaging Conventions],described, msopc/IOpcSigningOptions, opc.iopcsigningoptions
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
 - IOpcSigningOptions
 - msopc/IOpcSigningOptions
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
 - IOpcSigningOptions
---

# IOpcSigningOptions interface


## -description

Provides methods to set and access information required to generate a signature.

## -inheritance

The <b>IOpcSigningOptions</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcSigningOptions</b> also has these types of members:

## -remarks

To generate a signature, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignaturemanager-sign">IOpcDigitalSignatureManager::Sign</a> method with the <i>signingOptions</i> parameter value set to an <b>IOpcSigningOptions</b> interface pointer.

To create an <b>IOpcSigningOptions</b> interface pointer, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignaturemanager-createsigningoptions">IOpcDigitalSignatureManager::CreateSigningOptions</a> method.

The caller must set a default for the digest method and signature method before generating a signature. To set a default digest method, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-setdefaultdigestmethod">SetDefaultDigestMethod</a> method. To set a signature method, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-setsignaturemethod">SetSignatureMethod</a> method.

To get an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobjectset">IOpcSignatureCustomObjectSet</a> interface pointer, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-getcustomobjectset">GetCustomObjectSet</a> method. The interface pointers in the set represent application-specific <b>Object</b> elements.

 To get an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceset">IOpcSignatureReferenceSet</a> interface pointer, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-getcustomreferenceset">GetCustomReferenceSet</a> method. The interface pointers in the set represent references to application-specific <b>Object</b> elements or their children that will be signed when the signature is generated.

The default location of the certificate is <b>OPC_CERTIFICATE_IN_CERTIFICATE_PART</b>. To change this value, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-setcertificateembeddingoption">SetCertificateEmbeddingOption</a> method.

The default format of the signing time string is <b>OPC_SIGNATURE_TIME_FORMAT_MILLISECONDS</b>. To change the format of the signing time string, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-settimeformat">SetTimeFormat</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignaturemanager">IOpcDigitalSignatureManager</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
