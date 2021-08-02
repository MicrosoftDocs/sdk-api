---
UID: NN:msopc.IOpcRelationshipSelectorEnumerator
title: IOpcRelationshipSelectorEnumerator (msopc.h)
description: A read-only enumerator of IOpcRelationshipSelector interface pointers.
helpviewer_keywords: ["IOpcRelationshipSelectorEnumerator","IOpcRelationshipSelectorEnumerator interface [Open Packaging Conventions]","IOpcRelationshipSelectorEnumerator interface [Open Packaging Conventions]","described","msopc/IOpcRelationshipSelectorEnumerator","opc.iopcrelationshipselectorenumerator"]
old-location: opc\iopcrelationshipselectorenumerator.htm
tech.root: OPC
ms.assetid: 9c0bbc0d-d950-4929-9100-41a7f016a208
ms.date: 12/05/2018
ms.keywords: IOpcRelationshipSelectorEnumerator, IOpcRelationshipSelectorEnumerator interface [Open Packaging Conventions], IOpcRelationshipSelectorEnumerator interface [Open Packaging Conventions],described, msopc/IOpcRelationshipSelectorEnumerator, opc.iopcrelationshipselectorenumerator
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
 - IOpcRelationshipSelectorEnumerator
 - msopc/IOpcRelationshipSelectorEnumerator
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
 - IOpcRelationshipSelectorEnumerator
---

# IOpcRelationshipSelectorEnumerator interface


## -description

A read-only enumerator of <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselector">IOpcRelationshipSelector</a> interface pointers.

## -inheritance

The <b>IOpcRelationshipSelectorEnumerator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcRelationshipSelectorEnumerator</b> also has these types of members:

## -remarks

When an enumerator is created, the current position precedes the first pointer.

To set the current position to the first pointer of the enumerator, call the  <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipselectorenumerator-movenext">MoveNext</a> method after creating the enumerator.

Changes to the set will invalidate the enumerator, and all subsequent calls to it will fail.

To get an 
				 <b>IOpcRelationshipSelectorEnumerator</b> interface pointer, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipselectorset-getenumerator">IOpcRelationshipSelectorSet::GetEnumerator</a> or  <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreference-getrelationshipselectorenumerator">IOpcSignatureRelationshipReference::GetRelationshipSelectorEnumerator</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselectorset">IOpcRelationshipSelectorSet</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
