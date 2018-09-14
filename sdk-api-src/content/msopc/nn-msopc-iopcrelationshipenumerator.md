---
UID: NN:msopc.IOpcRelationshipEnumerator
title: IOpcRelationshipEnumerator
author: windows-sdk-content
description: A read-only enumerator of IOpcRelationship interface pointers.
old-location: opc\iopcrelationshipenumerator.htm
tech.root: OPC
ms.assetid: 8d8071cb-89ea-421e-9475-04a028317198
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IOpcRelationshipEnumerator, IOpcRelationshipEnumerator interface [Open Packaging Conventions], IOpcRelationshipEnumerator interface [Open Packaging Conventions],described, msopc/IOpcRelationshipEnumerator, opc.iopcrelationshipenumerator
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcRelationshipEnumerator interface


## -description


A read-only enumerator of <a href="https://msdn.microsoft.com/eb3619bb-470f-41bd-a231-d63df70592c2">IOpcRelationship</a> interface pointers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcRelationshipEnumerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpcRelationshipEnumerator</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/838f9486-be46-461f-b570-bc77003f1619">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the current enumerator and all its descendants.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ddd7a5f-659d-45e1-aff8-dee799efd8ac">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/eb3619bb-470f-41bd-a231-d63df70592c2">IOpcRelationship</a> interface pointer at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0733a11-0ba6-445f-8e3c-b62ad7b6b4bf">MoveNext</a>
</td>
<td align="left" width="63%">
Moves the current position of the enumerator to the next <a href="https://msdn.microsoft.com/eb3619bb-470f-41bd-a231-d63df70592c2">IOpcRelationship</a> interface pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ee69fea-b542-4c48-be4f-03595d227cde">MovePrevious</a>
</td>
<td align="left" width="63%">
Moves the current position of the enumerator to the previous <a href="https://msdn.microsoft.com/eb3619bb-470f-41bd-a231-d63df70592c2">IOpcRelationship</a> interface pointer.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call either the <a href="https://msdn.microsoft.com/bcffa20d-b86e-4bfe-9f67-7404d44acb03">IOpcRelationshipSet::GetEnumerator</a> or the <a href="https://msdn.microsoft.com/5b389660-f74d-48ae-a16b-5822661f0015">IOpcRelationshipSet::GetEnumeratorForType</a> method.

When an enumerator is created, the current position precedes the first pointer. To set the current position to the first pointer of the enumerator, call the  <a href="https://msdn.microsoft.com/d0733a11-0ba6-445f-8e3c-b62ad7b6b4bf">MoveNext</a>method after creating the enumerator.


<div class="alert"><b>Note</b>  Changes to the set will invalidate the enumerator, and all subsequent calls will fail.</div>
<div> </div>



#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/6259906d-820d-4b6e-bbeb-d9d044f2b35a">IOpcRelationshipSet</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<b>Reference</b>
 

 

