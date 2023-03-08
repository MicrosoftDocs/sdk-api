---
UID: NE:msopc.__MIDL___MIDL_itf_msopc_0000_0002_0001
title: OPC_URI_TARGET_MODE (msopc.h)
description: Indicates the target mode of a relationship.
helpviewer_keywords: ["OPC_URI_TARGET_MODE","OPC_URI_TARGET_MODE enumeration [Open Packaging Conventions]","OPC_URI_TARGET_MODE_EXTERNAL","OPC_URI_TARGET_MODE_INTERNAL","msopc/OPC_URI_TARGET_MODE","msopc/OPC_URI_TARGET_MODE_EXTERNAL","msopc/OPC_URI_TARGET_MODE_INTERNAL","opc.opc_uri_target_mode"]
old-location: opc\opc_uri_target_mode.htm
tech.root: OPC
ms.assetid: af052aa3-db7a-47de-938c-32895b8735e9
ms.date: 12/05/2018
ms.keywords: OPC_URI_TARGET_MODE, OPC_URI_TARGET_MODE enumeration [Open Packaging Conventions], OPC_URI_TARGET_MODE_EXTERNAL, OPC_URI_TARGET_MODE_INTERNAL, msopc/OPC_URI_TARGET_MODE, msopc/OPC_URI_TARGET_MODE_EXTERNAL, msopc/OPC_URI_TARGET_MODE_INTERNAL, opc.opc_uri_target_mode
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Opcbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OPC_URI_TARGET_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_msopc_0000_0002_0001
 - msopc/__MIDL___MIDL_itf_msopc_0000_0002_0001
 - OPC_URI_TARGET_MODE
 - msopc/OPC_URI_TARGET_MODE
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
 - OPC_URI_TARGET_MODE
---

# OPC_URI_TARGET_MODE enumeration


## -description

Indicates the target mode of a relationship.

## -enum-fields

### -field OPC_URI_TARGET_MODE_INTERNAL:0

The target of the relationship  is a part inside the package.

### -field OPC_URI_TARGET_MODE_EXTERNAL:1

The target of the relationship is a resource outside of the package.

## -remarks

If the relationship's  target mode is <b>OPC_URI_TARGET_MODE_INTERNAL</b> the URI of the target  part is relative to the URI of the source of the relationship.

To get the URI of the target of the relationship, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationship-gettargeturi">IOpcRelationship::GetTargetUri</a> method.

For more information about relationships, see the <a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a> and the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>.

## -see-also

<a href="https://www.ecma-international.org/publications/standards/Ecma-376.htm">ECMA-376 OpenXML standard</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a>



<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipset-createrelationship">IOpcRelationshipSet::CreateRelationship</a>



<a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-enumerations">Packaging Enumerations</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>



<a href="/previous-versions/windows/desktop/opc/relationships-overview">Relationships Overview</a>
