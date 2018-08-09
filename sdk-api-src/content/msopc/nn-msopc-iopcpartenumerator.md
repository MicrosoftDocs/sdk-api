---
UID: NN:msopc.IOpcPartEnumerator
title: IOpcPartEnumerator
author: windows-sdk-content
description: A read-only enumerator of IOpcPart interface pointers.
old-location: opc\iopcpartenumerator.htm
old-project: OPC
ms.assetid: 0a2296b2-a149-439a-abcf-2bc2eb6d1235
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IOpcPartEnumerator, IOpcPartEnumerator interface [Open Packaging Conventions], IOpcPartEnumerator interface [Open Packaging Conventions],described, msopc/IOpcPartEnumerator, opc.iopcpartenumerator
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
tech.root: 
req.typenames: OPC_SIGNATURE_TIME_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msopc.h
api_name:
 - IOpcPartEnumerator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcPartEnumerator interface


## -description


A read-only enumerator of <a href="https://msdn.microsoft.com/e6a40f30-03d1-4c93-a5e0-563b4c6588b4">IOpcPart</a> interface pointers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcPartEnumerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpcPartEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcPartEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the current enumerator and all its descendants.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54759fcb-858f-434c-92e9-6164f3d972fb">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/e6a40f30-03d1-4c93-a5e0-563b4c6588b4">IOpcPart</a> interface pointer at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4d52bb74-53f5-4c7c-a42e-5d67e330b48c">MoveNext</a>
</td>
<td align="left" width="63%">
Moves the current position of the enumerator to the next <a href="https://msdn.microsoft.com/e6a40f30-03d1-4c93-a5e0-563b4c6588b4">IOpcPart</a> interface pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6405bf6f-da60-463c-9acc-820b586e42e1">MovePrevious</a>
</td>
<td align="left" width="63%">
Moves the current position of the enumerator to the previous <a href="https://msdn.microsoft.com/e6a40f30-03d1-4c93-a5e0-563b4c6588b4">IOpcPart</a> interface pointer.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call the <a href="https://msdn.microsoft.com/7b2a5ae6-b3ac-49b5-a798-9fca450da6d1">IOpcPartSet::GetEnumerator</a> method.

When an enumerator is created, the current position precedes the first pointer. To set the current position to the first pointer of the enumerator, call the <a href="https://msdn.microsoft.com/4d52bb74-53f5-4c7c-a42e-5d67e330b48c">MoveNext</a>method after creating the enumerator.

<div class="alert"><b>Note</b>  Changes to the enumerator's underlying set will invalidate the enumerator, and all subsequent calls will fail.</div>
<div> </div>

#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/f34c682f-7677-4d20-bd37-b1a68293d85c">IOpcPartSet</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<b>Reference</b>
 

 

