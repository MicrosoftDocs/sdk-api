---
UID: NN:msopc.IOpcPartEnumerator
title: IOpcPartEnumerator (msopc.h)
description: A read-only enumerator of IOpcPart interface pointers.
helpviewer_keywords: ["IOpcPartEnumerator","IOpcPartEnumerator interface [Open Packaging Conventions]","IOpcPartEnumerator interface [Open Packaging Conventions]","described","msopc/IOpcPartEnumerator","opc.iopcpartenumerator"]
old-location: opc\iopcpartenumerator.htm
tech.root: OPC
ms.assetid: 0a2296b2-a149-439a-abcf-2bc2eb6d1235
ms.date: 12/05/2018
ms.keywords: IOpcPartEnumerator, IOpcPartEnumerator interface [Open Packaging Conventions], IOpcPartEnumerator interface [Open Packaging Conventions],described, msopc/IOpcPartEnumerator, opc.iopcpartenumerator
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
 - IOpcPartEnumerator
 - msopc/IOpcPartEnumerator
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
 - IOpcPartEnumerator
---

# IOpcPartEnumerator interface


## -description

A read-only enumerator of <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpart">IOpcPart</a> interface pointers.

## -inheritance

The <b>IOpcPartEnumerator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcPartEnumerator</b> also has these types of members:

## -remarks

To get a pointer to this interface, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcpartset-getenumerator">IOpcPartSet::GetEnumerator</a> method.

When an enumerator is created, the current position precedes the first pointer. To set the current position to the first pointer of the enumerator, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcpartenumerator-movenext">MoveNext</a> method after creating the enumerator.

<div class="alert"><b>Note</b>  Changes to the enumerator's underlying set will invalidate the enumerator, and all subsequent calls will fail.</div>
<div> </div>

#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpartset">IOpcPartSet</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<b>Reference</b>
