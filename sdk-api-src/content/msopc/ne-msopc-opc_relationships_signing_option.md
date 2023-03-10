---
UID: NE:msopc.__MIDL___MIDL_itf_msopc_0001_0076_0003
title: OPC_RELATIONSHIPS_SIGNING_OPTION (msopc.h)
description: Describes whether a reference represented by the IOpcSignatureRelationshipReference interface refers to all or a subset of relationships represented as relationship objects in a relationship set object.
helpviewer_keywords: ["OPC_RELATIONSHIPS_SIGNING_OPTION","OPC_RELATIONSHIPS_SIGNING_OPTION enumeration [Open Packaging Conventions]","OPC_RELATIONSHIP_SIGN_PART","OPC_RELATIONSHIP_SIGN_USING_SELECTORS","msopc/OPC_RELATIONSHIPS_SIGNING_OPTION","msopc/OPC_RELATIONSHIP_SIGN_PART","msopc/OPC_RELATIONSHIP_SIGN_USING_SELECTORS","opc.opc_relationships_signing_option"]
old-location: opc\opc_relationships_signing_option.htm
tech.root: OPC
ms.assetid: b6a83730-459a-4119-a013-7d670e659c32
ms.date: 12/05/2018
ms.keywords: OPC_RELATIONSHIPS_SIGNING_OPTION, OPC_RELATIONSHIPS_SIGNING_OPTION enumeration [Open Packaging Conventions], OPC_RELATIONSHIP_SIGN_PART, OPC_RELATIONSHIP_SIGN_USING_SELECTORS, msopc/OPC_RELATIONSHIPS_SIGNING_OPTION, msopc/OPC_RELATIONSHIP_SIGN_PART, msopc/OPC_RELATIONSHIP_SIGN_USING_SELECTORS, opc.opc_relationships_signing_option
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
req.typenames: OPC_RELATIONSHIPS_SIGNING_OPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_msopc_0001_0076_0003
 - msopc/__MIDL___MIDL_itf_msopc_0001_0076_0003
 - OPC_RELATIONSHIPS_SIGNING_OPTION
 - msopc/OPC_RELATIONSHIPS_SIGNING_OPTION
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
 - OPC_RELATIONSHIPS_SIGNING_OPTION
---

# OPC_RELATIONSHIPS_SIGNING_OPTION enumeration


## -description

Describes whether a reference represented by the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a> interface refers to all or a subset of relationships represented as relationship objects in a relationship set object.

## -enum-fields

### -field OPC_RELATIONSHIP_SIGN_USING_SELECTORS:0

The reference refers to a subset of relationships represented as relationship objects and identified using the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselectorset">IOpcRelationshipSelectorSet</a> interface.

### -field OPC_RELATIONSHIP_SIGN_PART:1

The reference refers to all of the relationships represented as relationship objects in the relationship set object.

## -see-also

<a href="https://www.ecma-international.org/publications/standards/Ecma-376.htm">ECMA-376 OpenXML standard</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreference-getrelationshipsigningoption">IOpcSignatureRelationshipReference::GetRelationshipSigningOption</a>



<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreferenceset-create">IOpcSignatureRelationshipReferenceSet::Create</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-enumerations">Packaging Enumerations</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
