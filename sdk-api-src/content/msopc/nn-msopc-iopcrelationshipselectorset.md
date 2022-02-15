---
UID: NN:msopc.IOpcRelationshipSelectorSet
title: IOpcRelationshipSelectorSet (msopc.h)
description: An unordered set of IOpcRelationshipSelector interface pointers that represent the selection criteria that is used to identify relationships for signing.
helpviewer_keywords: ["IOpcRelationshipSelectorSet","IOpcRelationshipSelectorSet interface [Open Packaging Conventions]","IOpcRelationshipSelectorSet interface [Open Packaging Conventions]","described","msopc/IOpcRelationshipSelectorSet","opc.iopcrelationshipselectorset"]
old-location: opc\iopcrelationshipselectorset.htm
tech.root: OPC
ms.assetid: cb23cbe2-764c-47e4-bd32-2791ddde9eee
ms.date: 12/05/2018
ms.keywords: IOpcRelationshipSelectorSet, IOpcRelationshipSelectorSet interface [Open Packaging Conventions], IOpcRelationshipSelectorSet interface [Open Packaging Conventions],described, msopc/IOpcRelationshipSelectorSet, opc.iopcrelationshipselectorset
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msopc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOpcRelationshipSelectorSet
 - msopc/IOpcRelationshipSelectorSet
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msopc.h
api_name:
 - IOpcRelationshipSelectorSet
---

# IOpcRelationshipSelectorSet interface


## -description

An unordered set of <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselector">IOpcRelationshipSelector</a> interface pointers  that represent the selection criteria that is used to identify relationships for signing. The subset is selected from the relationships stored in a Relationships part.

## -inheritance

The <b>IOpcRelationshipSelectorSet</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcRelationshipSelectorSet</b> also has these types of members:

## -remarks

Use the methods of the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselector">IOpcRelationshipSelector</a> interface pointers in the set to select relationships for signing.

To create an <b>IOpcRelationshipSelectorSet</b> interface pointer, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreferenceset-createrelationshipselectorset">IOpcSignatureRelationshipReference::CreateRelationshipSelectorSet</a> method.

When an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselector">IOpcRelationshipSelector</a> interface pointer is created and added to the set, the criterion it provides access to is saved when the package is saved.

When an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselector">IOpcRelationshipSelector</a> interface pointer is deleted from the set, the criterion it provides access to is not saved when the package is saved.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselectorenumerator">IOpcRelationshipSelectorEnumerator</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a>



<a href="/windows/win32/api/msopc/ne-msopc-opc_relationship_selector">OPC_RELATIONSHIP_SELECTOR</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
