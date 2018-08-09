---
UID: NE:msopc.__MIDL___MIDL_itf_msopc_0001_0076_0004
title: "__MIDL___MIDL_itf_msopc_0001_0076_0004"
author: windows-sdk-content
description: Describes the storage location of a certificate that is used in signing.
old-location: opc\opc_certificate_embedding_option.htm
old-project: OPC
ms.assetid: 4292a53b-33a2-431c-806a-7e8c96ecce40
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: OPC_CERTIFICATE_EMBEDDING_OPTION, OPC_CERTIFICATE_EMBEDDING_OPTION enumeration [Open Packaging Conventions], OPC_CERTIFICATE_IN_CERTIFICATE_PART, OPC_CERTIFICATE_IN_SIGNATURE_PART, OPC_CERTIFICATE_NOT_EMBEDDED, __MIDL___MIDL_itf_msopc_0001_0076_0004, msopc/OPC_CERTIFICATE_EMBEDDING_OPTION, msopc/OPC_CERTIFICATE_IN_CERTIFICATE_PART, msopc/OPC_CERTIFICATE_IN_SIGNATURE_PART, msopc/OPC_CERTIFICATE_NOT_EMBEDDED, opc.opc_certificate_embedding_option
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: OPC_CERTIFICATE_EMBEDDING_OPTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msopc.h
api_name:
 - OPC_CERTIFICATE_EMBEDDING_OPTION
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# __MIDL___MIDL_itf_msopc_0001_0076_0004 enumeration


## -description


Describes the storage location of a certificate that is used in signing.


## -enum-fields




### -field OPC_CERTIFICATE_IN_CERTIFICATE_PART

The certificate is stored in a part specific to the certificate.


### -field OPC_CERTIFICATE_IN_SIGNATURE_PART

The certificate is encoded within the signature markup in the Signature part.


### -field OPC_CERTIFICATE_NOT_EMBEDDED

The certificate is not stored in the package.

<div class="alert"><b>Important</b>  The certificate is contextual and understood between the signer and the verifier.</div>
<div> </div>

## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt484158">Certificates</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">ECMA-376 OpenXML standard</a>



<b>External Resources</b>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/86f83829-0507-4918-ae7f-71738f985068">IOpcSigningOptions::GetCertificateEmbeddingOption</a>



<a href="https://msdn.microsoft.com/afae4b98-c05f-4fa3-bb1e-f9f43ee86e64">IOpcSigningOptions::SetCertificateEmbeddingOption</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/c84246dd-f34b-40ea-8530-f93483445533">Packaging Enumerations</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>



<a href="http://go.microsoft.com/fwlink/p/?linkid=125240">W3C Recommendation, Canonical XML
Version 1.0</a>
 

 

