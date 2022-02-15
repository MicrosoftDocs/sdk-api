---
UID: NE:msopc.__MIDL___MIDL_itf_msopc_0001_0076_0001
title: OPC_CANONICALIZATION_METHOD (msopc.h)
description: Describes the canonicalization method to be applied to XML markup.
helpviewer_keywords: ["OPC_CANONICALIZATION_C14N","OPC_CANONICALIZATION_C14N_WITH_COMMENTS","OPC_CANONICALIZATION_METHOD","OPC_CANONICALIZATION_METHOD enumeration [Open Packaging Conventions]","OPC_CANONICALIZATION_NONE","msopc/OPC_CANONICALIZATION_C14N","msopc/OPC_CANONICALIZATION_C14N_WITH_COMMENTS","msopc/OPC_CANONICALIZATION_METHOD","msopc/OPC_CANONICALIZATION_NONE","opc.opc_canonicalization_method"]
old-location: opc\opc_canonicalization_method.htm
tech.root: OPC
ms.assetid: f8401d12-da2e-4b35-b473-ebe3d1f91abd
ms.date: 12/05/2018
ms.keywords: OPC_CANONICALIZATION_C14N, OPC_CANONICALIZATION_C14N_WITH_COMMENTS, OPC_CANONICALIZATION_METHOD, OPC_CANONICALIZATION_METHOD enumeration [Open Packaging Conventions], OPC_CANONICALIZATION_NONE, msopc/OPC_CANONICALIZATION_C14N, msopc/OPC_CANONICALIZATION_C14N_WITH_COMMENTS, msopc/OPC_CANONICALIZATION_METHOD, msopc/OPC_CANONICALIZATION_NONE, opc.opc_canonicalization_method
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
req.typenames: OPC_CANONICALIZATION_METHOD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_msopc_0001_0076_0001
 - msopc/__MIDL___MIDL_itf_msopc_0001_0076_0001
 - OPC_CANONICALIZATION_METHOD
 - msopc/OPC_CANONICALIZATION_METHOD
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
 - OPC_CANONICALIZATION_METHOD
---

# OPC_CANONICALIZATION_METHOD enumeration


## -description

Describes the canonicalization method  to be applied to XML markup.

## -enum-fields

### -field OPC_CANONICALIZATION_NONE:0

No canonicalization method is applied.

### -field OPC_CANONICALIZATION_C14N:1

The C14N canonicalization method that removes comments is applied.

### -field OPC_CANONICALIZATION_C14N_WITH_COMMENTS:2

The C14N canonicalization method that preserves comments is applied.

## -remarks

For more information about XML canonicalization, see the <a href="https://www.w3.org/TR/xml-c14n">W3C Recommendation, Canonical XML
Version 1.0</a> (http://www.w3.org/TR/xml-c14n).

For more information about canonicalization and packages, see the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>.

## -see-also

<a href="https://www.ecma-international.org/publications/standards/Ecma-376.htm">ECMA-376 OpenXML standard</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getcanonicalizationmethod">IOpcDigitalSignature::GetCanonicalizationMethod</a>



<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturepartreference-gettransformmethod">IOpcSignaturePartReference::GetTransformMethod</a>



<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturepartreferenceset-create">IOpcSignaturePartReferenceSet::Create</a>



<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturereference-gettransformmethod">IOpcSignatureReference::GetTransformMethod</a>



<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturereferenceset-create">IOpcSignatureReferenceSet::Create</a>



<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreference-gettransformmethod">IOpcSignatureRelationshipReference::GetTransformMethod</a>



<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreferenceset-create">IOpcSignatureRelationshipReferenceSet::Create</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-enumerations">Packaging Enumerations</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>



<a href="https://www.w3.org/TR/xml-c14n">W3C Recommendation, Canonical XML
Version 1.0</a>
