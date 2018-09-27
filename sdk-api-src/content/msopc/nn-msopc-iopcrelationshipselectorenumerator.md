---
UID: NN:msopc.IOpcRelationshipSelectorEnumerator
title: IOpcRelationshipSelectorEnumerator
author: windows-sdk-content
description: A read-only enumerator of IOpcRelationshipSelector interface pointers.
old-location: opc\iopcrelationshipselectorenumerator.htm
tech.root: OPC
ms.assetid: 9c0bbc0d-d950-4929-9100-41a7f016a208
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IOpcRelationshipSelectorEnumerator, IOpcRelationshipSelectorEnumerator interface [Open Packaging Conventions], IOpcRelationshipSelectorEnumerator interface [Open Packaging Conventions],described, msopc/IOpcRelationshipSelectorEnumerator, opc.iopcrelationshipselectorenumerator
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
 - IOpcRelationshipSelectorEnumerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcRelationshipSelectorEnumerator interface


## -description


A read-only enumerator of <a href="https://msdn.microsoft.com/077f37c3-76af-4b96-9e3a-9fd9b865d941">IOpcRelationshipSelector</a> interface pointers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcRelationshipSelectorEnumerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpcRelationshipSelectorEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcRelationshipSelectorEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3eaf4b51-201d-43de-a9b7-408306992629">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the current <b>IOpcRelationshipSelectorEnumerator</b>interface pointer and all its descendants.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ffff6b7e-8e46-4be6-921f-b98e7d51a114">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/077f37c3-76af-4b96-9e3a-9fd9b865d941">IOpcRelationshipSelector</a> interface pointer at the current position of the enumerator.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a958f62d-3e9a-47d9-8ac2-a92a21a74ed1">MoveNext</a>
</td>
<td align="left" width="63%">
Moves the current position of the enumerator to the next <a href="https://msdn.microsoft.com/077f37c3-76af-4b96-9e3a-9fd9b865d941">IOpcRelationshipSelector</a>interface pointer.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd367eb8-cd1c-4f0a-a435-aad86685b71a">MovePrevious</a>
</td>
<td align="left" width="63%">
Moves the current position of the enumerator to the previous <a href="https://msdn.microsoft.com/077f37c3-76af-4b96-9e3a-9fd9b865d941">IOpcRelationshipSelector</a>interface pointer.
            

</td>
</tr>
</table> 


## -remarks



When an enumerator is created, the current position precedes the first pointer.

To set the current position to the first pointer of the enumerator, call the  <a href="https://msdn.microsoft.com/a958f62d-3e9a-47d9-8ac2-a92a21a74ed1">MoveNext</a>method after creating the enumerator.

Changes to the set will invalidate the enumerator, and all subsequent calls to it will fail.

To get an 
				 <b>IOpcRelationshipSelectorEnumerator</b> interface pointer, call the <a href="https://msdn.microsoft.com/7c0a885a-8ee2-40fe-bbc6-d7036e4a4c40">IOpcRelationshipSelectorSet::GetEnumerator</a> or  <a href="https://msdn.microsoft.com/a9e1e9e8-d318-4e72-ba52-d020e58f85ff">IOpcSignatureRelationshipReference::GetRelationshipSelectorEnumerator</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/cb23cbe2-764c-47e4-bd32-2791ddde9eee">IOpcRelationshipSelectorSet</a>



<a href="https://msdn.microsoft.com/24aebfff-6b4f-49cb-988f-670ffed7d815">IOpcSignatureRelationshipReference</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

