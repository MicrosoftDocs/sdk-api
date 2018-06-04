---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

