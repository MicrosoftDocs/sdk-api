---
UID: NN:msopc.IOpcRelationshipEnumerator
title: IOpcRelationshipEnumerator (msopc.h)
description: A read-only enumerator of IOpcRelationship interface pointers.helpviewer_keywords: ["IOpcRelationshipEnumerator","IOpcRelationshipEnumerator interface [Open Packaging Conventions]","IOpcRelationshipEnumerator interface [Open Packaging Conventions]","described","msopc/IOpcRelationshipEnumerator","opc.iopcrelationshipenumerator"]
old-location: opc\iopcrelationshipenumerator.htm
tech.root: OPC
ms.assetid: 8d8071cb-89ea-421e-9475-04a028317198
ms.date: 12/05/2018
ms.keywords: IOpcRelationshipEnumerator, IOpcRelationshipEnumerator interface [Open Packaging Conventions], IOpcRelationshipEnumerator interface [Open Packaging Conventions],described, msopc/IOpcRelationshipEnumerator, opc.iopcrelationshipenumerator
f1_keywords:
- msopc/IOpcRelationshipEnumerator
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- msopc.h
api_name:
- IOpcRelationshipEnumerator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOpcRelationshipEnumerator interface


## -description


A read-only enumerator of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface pointers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcRelationshipEnumerator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcRelationshipEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcRelationshipEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipenumerator-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the current enumerator and all its descendants.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipenumerator-getcurrent">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface pointer at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipenumerator-movenext">MoveNext</a>
</td>
<td align="left" width="63%">
Moves the current position of the enumerator to the next <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipenumerator-moveprevious">MovePrevious</a>
</td>
<td align="left" width="63%">
Moves the current position of the enumerator to the previous <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface pointer.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call either the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipset-getenumerator">IOpcRelationshipSet::GetEnumerator</a> or the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipset-getenumeratorfortype">IOpcRelationshipSet::GetEnumeratorForType</a> method.

When an enumerator is created, the current position precedes the first pointer. To set the current position to the first pointer of the enumerator, call the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipenumerator-movenext">MoveNext</a>method after creating the enumerator.


<div class="alert"><b>Note</b>  Changes to the set will invalidate the enumerator, and all subsequent calls will fail.</div>
<div> </div>



#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipset">IOpcRelationshipSet</a>



<b>Overviews</b>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<b>Reference</b>
 

 

