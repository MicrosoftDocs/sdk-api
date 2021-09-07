---
UID: NN:msopc.IOpcSignatureReferenceEnumerator
title: IOpcSignatureReferenceEnumerator (msopc.h)
description: A read-only enumerator of IOpcSignatureReference interface pointers.
helpviewer_keywords: ["IOpcSignatureReferenceEnumerator","IOpcSignatureReferenceEnumerator interface [Open Packaging Conventions]","IOpcSignatureReferenceEnumerator interface [Open Packaging Conventions]","described","msopc/IOpcSignatureReferenceEnumerator","opc.iopcsignaturereferenceenumerator"]
old-location: opc\iopcsignaturereferenceenumerator.htm
tech.root: OPC
ms.assetid: 1d0a14c6-826c-419f-9e94-d5929fdbae82
ms.date: 12/05/2018
ms.keywords: IOpcSignatureReferenceEnumerator, IOpcSignatureReferenceEnumerator interface [Open Packaging Conventions], IOpcSignatureReferenceEnumerator interface [Open Packaging Conventions],described, msopc/IOpcSignatureReferenceEnumerator, opc.iopcsignaturereferenceenumerator
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
 - IOpcSignatureReferenceEnumerator
 - msopc/IOpcSignatureReferenceEnumerator
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
 - IOpcSignatureReferenceEnumerator
---

# IOpcSignatureReferenceEnumerator interface


## -description

A read-only enumerator of <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereference">IOpcSignatureReference</a> interface pointers.

## -inheritance

The <b>IOpcSignatureReferenceEnumerator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcSignatureReferenceEnumerator</b> also has these types of members:

## -remarks

When an enumerator is created, the current position precedes the first pointer. To set the current position to the first pointer of the enumerator, call the  <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturereferenceenumerator-movenext">MoveNext</a> method after creating the enumerator.

Changes to the set will invalidate the enumerator, and all subsequent calls to it will fail.

To get an <b>IOpcSignatureReferenceEnumerator</b> interface pointer, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturereferenceset-getenumerator">IOpcSignatureReferenceSet::GetEnumerator</a> or <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getcustomreferenceenumerator">IOpcDigitalSignature::GetCustomReferenceEnumerator</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceset">IOpcSignatureReferenceSet</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
