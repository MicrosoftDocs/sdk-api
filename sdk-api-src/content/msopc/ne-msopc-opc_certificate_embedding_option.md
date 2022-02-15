---
UID: NE:msopc.__MIDL___MIDL_itf_msopc_0001_0076_0004
title: OPC_CERTIFICATE_EMBEDDING_OPTION (msopc.h)
description: Describes the storage location of a certificate that is used in signing.
helpviewer_keywords: ["OPC_CERTIFICATE_EMBEDDING_OPTION","OPC_CERTIFICATE_EMBEDDING_OPTION enumeration [Open Packaging Conventions]","OPC_CERTIFICATE_IN_CERTIFICATE_PART","OPC_CERTIFICATE_IN_SIGNATURE_PART","OPC_CERTIFICATE_NOT_EMBEDDED","msopc/OPC_CERTIFICATE_EMBEDDING_OPTION","msopc/OPC_CERTIFICATE_IN_CERTIFICATE_PART","msopc/OPC_CERTIFICATE_IN_SIGNATURE_PART","msopc/OPC_CERTIFICATE_NOT_EMBEDDED","opc.opc_certificate_embedding_option"]
old-location: opc\opc_certificate_embedding_option.htm
tech.root: OPC
ms.assetid: 4292a53b-33a2-431c-806a-7e8c96ecce40
ms.date: 12/05/2018
ms.keywords: OPC_CERTIFICATE_EMBEDDING_OPTION, OPC_CERTIFICATE_EMBEDDING_OPTION enumeration [Open Packaging Conventions], OPC_CERTIFICATE_IN_CERTIFICATE_PART, OPC_CERTIFICATE_IN_SIGNATURE_PART, OPC_CERTIFICATE_NOT_EMBEDDED, msopc/OPC_CERTIFICATE_EMBEDDING_OPTION, msopc/OPC_CERTIFICATE_IN_CERTIFICATE_PART, msopc/OPC_CERTIFICATE_IN_SIGNATURE_PART, msopc/OPC_CERTIFICATE_NOT_EMBEDDED, opc.opc_certificate_embedding_option
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: OPC_CERTIFICATE_EMBEDDING_OPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_msopc_0001_0076_0004
 - msopc/__MIDL___MIDL_itf_msopc_0001_0076_0004
 - OPC_CERTIFICATE_EMBEDDING_OPTION
 - msopc/OPC_CERTIFICATE_EMBEDDING_OPTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msopc.h
api_name:
 - OPC_CERTIFICATE_EMBEDDING_OPTION
---

# OPC_CERTIFICATE_EMBEDDING_OPTION enumeration


## -description

Describes the storage location of a certificate that is used in signing.

## -enum-fields

### -field OPC_CERTIFICATE_IN_CERTIFICATE_PART:0

The certificate is stored in a part specific to the certificate.

### -field OPC_CERTIFICATE_IN_SIGNATURE_PART:1

The certificate is encoded within the signature markup in the Signature part.

### -field OPC_CERTIFICATE_NOT_EMBEDDED:2

The certificate is not stored in the package.

<div class="alert"><b>Important</b>  The certificate is contextual and understood between the signer and the verifier.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/SecCrypto/certificates">Certificates</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="https://www.ecma-international.org/publications/standards/Ecma-376.htm">ECMA-376 OpenXML standard</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-getcertificateembeddingoption">IOpcSigningOptions::GetCertificateEmbeddingOption</a>



<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-setcertificateembeddingoption">IOpcSigningOptions::SetCertificateEmbeddingOption</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-enumerations">Packaging Enumerations</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>



<a href="https://www.w3.org/TR/xml-c14n">W3C Recommendation, Canonical XML
Version 1.0</a>
