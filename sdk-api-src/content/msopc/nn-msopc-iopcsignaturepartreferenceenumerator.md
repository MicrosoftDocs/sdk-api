---
UID: NN:msopc.IOpcSignaturePartReferenceEnumerator
title: IOpcSignaturePartReferenceEnumerator (msopc.h)
description: A read-only enumerator of IOpcSignaturePartReference interface pointers.
helpviewer_keywords: ["IOpcSignaturePartReferenceEnumerator","IOpcSignaturePartReferenceEnumerator interface [Open Packaging Conventions]","IOpcSignaturePartReferenceEnumerator interface [Open Packaging Conventions]","described","msopc/IOpcSignaturePartReferenceEnumerator","opc.iopcsignaturepartreferenceenumerator"]
old-location: opc\iopcsignaturepartreferenceenumerator.htm
tech.root: OPC
ms.assetid: 8a54debe-3ac6-471d-b5a5-c3512da4d079
ms.date: 12/05/2018
ms.keywords: IOpcSignaturePartReferenceEnumerator, IOpcSignaturePartReferenceEnumerator interface [Open Packaging Conventions], IOpcSignaturePartReferenceEnumerator interface [Open Packaging Conventions],described, msopc/IOpcSignaturePartReferenceEnumerator, opc.iopcsignaturepartreferenceenumerator
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IOpcSignaturePartReferenceEnumerator
 - msopc/IOpcSignaturePartReferenceEnumerator
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
 - IOpcSignaturePartReferenceEnumerator
---

# IOpcSignaturePartReferenceEnumerator interface


## -description

A read-only enumerator of <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturepartreference">IOpcSignaturePartReference</a> interface pointers.

## -inheritance

The <b>IOpcSignaturePartReferenceEnumerator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcSignaturePartReferenceEnumerator</b> also has these types of members:

## -remarks

When an enumerator is created, the current position precedes the first pointer. To set the current position to the first pointer of the enumerator, call the  <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturepartreferenceenumerator-movenext">MoveNext</a> method after creating the enumerator.

Changes to the set will invalidate the enumerator, and all subsequent calls to it will fail.

To get an <b>IOpcSignaturePartReferenceEnumerator</b> interface pointer, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturepartreferenceset-getenumerator">IOpcSignaturePartReferenceSet::GetEnumerator</a> or <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getsignaturepartreferenceenumerator">IOpcDigitalSignature::GetSignaturePartReferenceEnumerator</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturepartreferenceset">IOpcSignaturePartReferenceSet</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
