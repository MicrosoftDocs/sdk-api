---
UID: NE:msopc.__MIDL___MIDL_itf_msopc_0001_0076_0001
title: OPC_CANONICALIZATION_METHOD (msopc.h)
author: windows-sdk-content
description: Describes the canonicalization method to be applied to XML markup.
old-location: opc\opc_canonicalization_method.htm
tech.root: OPC
ms.assetid: f8401d12-da2e-4b35-b473-ebe3d1f91abd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: OPC_CANONICALIZATION_C14N, OPC_CANONICALIZATION_C14N_WITH_COMMENTS, OPC_CANONICALIZATION_METHOD, OPC_CANONICALIZATION_METHOD enumeration [Open Packaging Conventions], OPC_CANONICALIZATION_NONE, msopc/OPC_CANONICALIZATION_C14N, msopc/OPC_CANONICALIZATION_C14N_WITH_COMMENTS, msopc/OPC_CANONICALIZATION_METHOD, msopc/OPC_CANONICALIZATION_NONE, opc.opc_canonicalization_method
ms.topic: enum
f1_keywords: 
 - "msopc/OPC_CANONICALIZATION_METHOD"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msopc.h
api_name:
 - OPC_CANONICALIZATION_METHOD
targetos: Windows
req.typenames: OPC_CANONICALIZATION_METHOD
req.redist: 
ms.custom: 19H1
---

# OPC_CANONICALIZATION_METHOD enumeration


## -description


Describes the canonicalization method  to be applied to XML markup.


## -enum-fields




### -field OPC_CANONICALIZATION_NONE

No canonicalization method is applied.


### -field OPC_CANONICALIZATION_C14N

The C14N canonicalization method that removes comments is applied.


### -field OPC_CANONICALIZATION_C14N_WITH_COMMENTS

The C14N canonicalization method that preserves comments is applied.


## -remarks



For more information about XML canonicalization, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=125240">W3C Recommendation, Canonical XML
Version 1.0</a> (http://go.microsoft.com/fwlink/p/?linkid=125240).

For more information about canonicalization and packages, see the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">ECMA-376 OpenXML standard</a>



<b>External Resources</b>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getcanonicalizationmethod">IOpcDigitalSignature::GetCanonicalizationMethod</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturepartreference-gettransformmethod">IOpcSignaturePartReference::GetTransformMethod</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturepartreferenceset-create">IOpcSignaturePartReferenceSet::Create</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturereference-gettransformmethod">IOpcSignatureReference::GetTransformMethod</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturereferenceset-create">IOpcSignatureReferenceSet::Create</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreference-gettransformmethod">IOpcSignatureRelationshipReference::GetTransformMethod</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreferenceset-create">IOpcSignatureRelationshipReferenceSet::Create</a>



<b>Overviews</b>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-enumerations">Packaging Enumerations</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>



<a href="http://go.microsoft.com/fwlink/p/?linkid=125240">W3C Recommendation, Canonical XML
Version 1.0</a>
 

 

