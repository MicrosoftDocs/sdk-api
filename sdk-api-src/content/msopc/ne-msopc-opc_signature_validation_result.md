---
UID: NE:msopc.OPC_SIGNATURE_VALIDATION_RESULT
title: OPC_SIGNATURE_VALIDATION_RESULT
author: windows-sdk-content
description: Indicates the status of the signature.
old-location: opc\opc_signature_validation_result.htm
old-project: OPC
ms.assetid: 991e0620-d674-4c2c-b0d8-18d7fdd031fb
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: OPC_SIGNATURE_INVALID, OPC_SIGNATURE_VALID, OPC_SIGNATURE_VALIDATION_RESULT, OPC_SIGNATURE_VALIDATION_RESULT enumeration [Open Packaging Conventions], msopc/OPC_SIGNATURE_INVALID, msopc/OPC_SIGNATURE_VALID, msopc/OPC_SIGNATURE_VALIDATION_RESULT, opc.opc_signature_validation_result
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
req.typenames: OPC_SIGNATURE_VALIDATION_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msopc.h
api_name:
 - OPC_SIGNATURE_VALIDATION_RESULT
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# OPC_SIGNATURE_VALIDATION_RESULT enumeration


## -description


Indicates the status of the signature.


## -enum-fields




### -field OPC_SIGNATURE_VALID

The signature is valid.

Signature validation using the provided certificate succeeded; signed package components have not been altered.

<div class="alert"><b>Important</b>  Signature trust decisions must be based on the validity of the signature  as well as other format- and application-specific factors, including:  validation of the identity of the package originator, signing policy, certificate quality, and possibly the existence of a valid time stamp.</div>
<div> </div>

### -field OPC_SIGNATURE_INVALID

The signature is not valid.

Signature markup or signed package components might have been altered. Alternatively, the signature might not exist in the current package.


## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">ECMA-376 OpenXML standard</a>



<b>External Resources</b>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/c84246dd-f34b-40ea-8530-f93483445533">Packaging Enumerations</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>



<a href="http://go.microsoft.com/fwlink/p/?linkid=132847">W3C Recommendation, XML Signature and Syntax Processing</a>
 

 

