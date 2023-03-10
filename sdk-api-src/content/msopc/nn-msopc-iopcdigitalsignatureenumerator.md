---
UID: NN:msopc.IOpcDigitalSignatureEnumerator
title: IOpcDigitalSignatureEnumerator (msopc.h)
description: A read-only enumerator of IOpcDigitalSignature interface pointers.
helpviewer_keywords: ["IOpcDigitalSignatureEnumerator","IOpcDigitalSignatureEnumerator interface [Open Packaging Conventions]","IOpcDigitalSignatureEnumerator interface [Open Packaging Conventions]","described","msopc/IOpcDigitalSignatureEnumerator","opc.iopcdigitalsignatureenumerator"]
old-location: opc\iopcdigitalsignatureenumerator.htm
tech.root: OPC
ms.assetid: 73fd0e47-7503-470d-b649-e4b2ba492bf1
ms.date: 12/05/2018
ms.keywords: IOpcDigitalSignatureEnumerator, IOpcDigitalSignatureEnumerator interface [Open Packaging Conventions], IOpcDigitalSignatureEnumerator interface [Open Packaging Conventions],described, msopc/IOpcDigitalSignatureEnumerator, opc.iopcdigitalsignatureenumerator
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
 - IOpcDigitalSignatureEnumerator
 - msopc/IOpcDigitalSignatureEnumerator
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
 - IOpcDigitalSignatureEnumerator
---

# IOpcDigitalSignatureEnumerator interface


## -description

A read-only enumerator of <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a> interface pointers.

## -inheritance

The <b>IOpcDigitalSignatureEnumerator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcDigitalSignatureEnumerator</b> also has these types of members:

## -remarks

When an enumerator is created, the current position precedes the first pointer. To set the current position to the first pointer of the enumerator, call the  <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignatureenumerator-movenext">MoveNext</a> method after creating the enumerator.

Changes to the set will invalidate the enumerator and all subsequent calls to it will fail.

To get an   <b>IOpcDigitalSignatureEnumerator</b> interface pointer, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignaturemanager-getsignatureenumerator">IOpcDigitalSignatureManager::GetSignatureEnumerator</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignaturemanager">IOpcDigitalSignatureManager</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
