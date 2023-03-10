---
UID: NE:msopc.__MIDL___MIDL_itf_msopc_0001_0076_0002
title: OPC_RELATIONSHIP_SELECTOR (msopc.h)
description: Describes how to interpret the selectionCriterion parameter of the IOpcRelationshipSelector::GetSelectionCriterion method.
helpviewer_keywords: ["OPC_RELATIONSHIP_SELECTOR","OPC_RELATIONSHIP_SELECTOR enumeration [Open Packaging Conventions]","OPC_RELATIONSHIP_SELECT_BY_ID","OPC_RELATIONSHIP_SELECT_BY_TYPE","msopc/OPC_RELATIONSHIP_SELECTOR","msopc/OPC_RELATIONSHIP_SELECT_BY_ID","msopc/OPC_RELATIONSHIP_SELECT_BY_TYPE","opc.opc_relationship_selector"]
old-location: opc\opc_relationship_selector.htm
tech.root: OPC
ms.assetid: 5532aab1-850e-4de8-a470-c55fb4c2f8c4
ms.date: 12/05/2018
ms.keywords: OPC_RELATIONSHIP_SELECTOR, OPC_RELATIONSHIP_SELECTOR enumeration [Open Packaging Conventions], OPC_RELATIONSHIP_SELECT_BY_ID, OPC_RELATIONSHIP_SELECT_BY_TYPE, msopc/OPC_RELATIONSHIP_SELECTOR, msopc/OPC_RELATIONSHIP_SELECT_BY_ID, msopc/OPC_RELATIONSHIP_SELECT_BY_TYPE, opc.opc_relationship_selector
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
req.typenames: OPC_RELATIONSHIP_SELECTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_msopc_0001_0076_0002
 - msopc/__MIDL___MIDL_itf_msopc_0001_0076_0002
 - OPC_RELATIONSHIP_SELECTOR
 - msopc/OPC_RELATIONSHIP_SELECTOR
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
 - OPC_RELATIONSHIP_SELECTOR
---

# OPC_RELATIONSHIP_SELECTOR enumeration


## -description

Describes how to interpret the  <i>selectionCriterion</i> parameter of the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipselector-getselectioncriterion">IOpcRelationshipSelector::GetSelectionCriterion</a> method.

## -enum-fields

### -field OPC_RELATIONSHIP_SELECT_BY_ID:0

The <i>selectionCriterion</i> parameter is a relationship identifier.

### -field OPC_RELATIONSHIP_SELECT_BY_TYPE:1

The <i>selectionCriterion</i> parameter is a relationship type.

## -see-also

<a href="https://www.ecma-international.org/publications/standards/Ecma-376.htm">ECMA-376 OpenXML standard</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipselector-getselectortype">IOpcRelationshipSelector::GetSelectorType</a>



<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipselectorset-create">IOpcRelationshipSelectorSet::Create</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-enumerations">Packaging Enumerations</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
