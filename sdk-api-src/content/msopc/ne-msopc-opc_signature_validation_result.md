---
UID: NE:msopc.OPC_SIGNATURE_VALIDATION_RESULT
title: OPC_SIGNATURE_VALIDATION_RESULT (msopc.h)
description: Indicates the status of the signature.
helpviewer_keywords: ["OPC_SIGNATURE_INVALID","OPC_SIGNATURE_VALID","OPC_SIGNATURE_VALIDATION_RESULT","OPC_SIGNATURE_VALIDATION_RESULT enumeration [Open Packaging Conventions]","msopc/OPC_SIGNATURE_INVALID","msopc/OPC_SIGNATURE_VALID","msopc/OPC_SIGNATURE_VALIDATION_RESULT","opc.opc_signature_validation_result"]
old-location: opc\opc_signature_validation_result.htm
tech.root: OPC
ms.assetid: 991e0620-d674-4c2c-b0d8-18d7fdd031fb
ms.date: 12/05/2018
ms.keywords: OPC_SIGNATURE_INVALID, OPC_SIGNATURE_VALID, OPC_SIGNATURE_VALIDATION_RESULT, OPC_SIGNATURE_VALIDATION_RESULT enumeration [Open Packaging Conventions], msopc/OPC_SIGNATURE_INVALID, msopc/OPC_SIGNATURE_VALID, msopc/OPC_SIGNATURE_VALIDATION_RESULT, opc.opc_signature_validation_result
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
req.typenames: OPC_SIGNATURE_VALIDATION_RESULT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OPC_SIGNATURE_VALIDATION_RESULT
 - msopc/OPC_SIGNATURE_VALIDATION_RESULT
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
 - OPC_SIGNATURE_VALIDATION_RESULT
---

# OPC_SIGNATURE_VALIDATION_RESULT enumeration


## -description

Indicates the status of the signature.

## -enum-fields

### -field OPC_SIGNATURE_VALID:0

The signature is valid.

Signature validation using the provided certificate succeeded; signed package components have not been altered.

<div class="alert"><b>Important</b>  Signature trust decisions must be based on the validity of the signature  as well as other format- and application-specific factors, including:  validation of the identity of the package originator, signing policy, certificate quality, and possibly the existence of a valid time stamp.</div>
<div> </div>

### -field OPC_SIGNATURE_INVALID:-1

The signature is not valid.

Signature markup or signed package components might have been altered. Alternatively, the signature might not exist in the current package.

## -see-also

<a href="https://www.ecma-international.org/publications/standards/Ecma-376.htm">ECMA-376 OpenXML standard</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-enumerations">Packaging Enumerations</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>



<a href="https://www.w3.org/TR/xmldsig-core/">W3C Recommendation, XML Signature and Syntax Processing</a>
