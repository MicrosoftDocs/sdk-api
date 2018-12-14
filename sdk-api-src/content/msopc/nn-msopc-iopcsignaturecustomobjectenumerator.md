---
UID: NN:msopc.IOpcSignatureCustomObjectEnumerator
title: IOpcSignatureCustomObjectEnumerator
author: windows-sdk-content
description: A read-only enumerator of IOpcSignatureCustomObject interface pointers.
old-location: opc\iopcsignaturecustomobjectenumerator.htm
tech.root: OPC
ms.assetid: e82caa1e-4cf8-457f-86d9-24f707544199
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IOpcSignatureCustomObjectEnumerator, IOpcSignatureCustomObjectEnumerator interface [Open Packaging Conventions], IOpcSignatureCustomObjectEnumerator interface [Open Packaging Conventions],described, msopc/IOpcSignatureCustomObjectEnumerator, opc.iopcsignaturecustomobjectenumerator
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IOpcSignatureCustomObjectEnumerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcSignatureCustomObjectEnumerator interface


## -description


A read-only enumerator of <a href="https://msdn.microsoft.com/4ebb4fbe-66cc-46d9-b548-31177d9f6da9">IOpcSignatureCustomObject</a> interface pointers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcSignatureCustomObjectEnumerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpcSignatureCustomObjectEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcSignatureCustomObjectEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51dd3758-26c6-4d4f-a956-61a9ff1f67c5">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the current <b>IOpcSignatureCustomObjectEnumerator</b> interface pointer and all its descendants.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a0197da5-e613-4aba-8098-901e192051ff">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/4ebb4fbe-66cc-46d9-b548-31177d9f6da9">IOpcSignatureCustomObject</a> interface at the current position of the enumerator.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b74d1e3-0a57-407c-bf05-f17aa84923e5">MoveNext</a>
</td>
<td align="left" width="63%">
Moves the current position of the enumerator to the next <a href="https://msdn.microsoft.com/4ebb4fbe-66cc-46d9-b548-31177d9f6da9">IOpcSignatureCustomObject</a> interface pointer.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1143280b-4c92-44cf-8e2d-acd26527f264">MovePrevious</a>
</td>
<td align="left" width="63%">
Moves the current position of the enumerator to the previous <a href="https://msdn.microsoft.com/4ebb4fbe-66cc-46d9-b548-31177d9f6da9">IOpcSignatureCustomObject</a>interface pointer.
            

</td>
</tr>
</table> 


## -remarks



When an enumerator is created, the current position precedes the first pointer of the enumerator. To set the current position to the first pointer, call the  <a href="https://msdn.microsoft.com/8b74d1e3-0a57-407c-bf05-f17aa84923e5">MoveNext</a>method after creating the enumerator.

Changes to the set will invalidate the enumerator, and all subsequent calls to it will fail.

To get an <b>IOpcSignatureCustomObjectEnumerator</b> interface pointer, call the <a href="https://msdn.microsoft.com/1263ca86-8b4f-4be9-a88a-f11e76178d0d">IOpcDigitalSignature::GetCustomObjectEnumerator</a> or <a href="https://msdn.microsoft.com/a365a1df-4c72-44a0-bcf5-8ef19c54f4ee">IOpcSignatureCustomObjectSet::GetEnumerator</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/cfa38ef6-9d96-4577-a3bf-518784d19ad8">IOpcDigitalSignature</a>



<a href="https://msdn.microsoft.com/eb2a561d-2723-45dc-98a6-ecf11101016b">IOpcSignatureCustomObjectSet</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

