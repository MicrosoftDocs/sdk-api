---
UID: NN:msopc.IOpcSignatureReferenceEnumerator
title: IOpcSignatureReferenceEnumerator
author: windows-driver-content
description: A read-only enumerator of IOpcSignatureReference interface pointers.
old-location: opc\iopcsignaturereferenceenumerator.htm
old-project: OPC
ms.assetid: 1d0a14c6-826c-419f-9e94-d5929fdbae82
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IOpcSignatureReferenceEnumerator, IOpcSignatureReferenceEnumerator interface [Open Packaging Conventions], IOpcSignatureReferenceEnumerator interface [Open Packaging Conventions],described, msopc/IOpcSignatureReferenceEnumerator, opc.iopcsignaturereferenceenumerator
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: OPC_SIGNATURE_TIME_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msopc.h
api_name:
-	IOpcSignatureReferenceEnumerator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IOpcSignatureReferenceEnumerator interface


## -description



	   A read-only enumerator of <a href="https://msdn.microsoft.com/2ce40bc7-754a-4f69-9348-75603e2257a4">IOpcSignatureReference</a> interface pointers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcSignatureReferenceEnumerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpcSignatureReferenceEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcSignatureReferenceEnumerator</b> interface has these methods.
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
Creates a copy of the current <b>IOpcSignatureReferenceEnumerator</b> interface pointer and all its descendants.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3bbf1a09-4d59-466f-ac48-2e4e67232ed4">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/2ce40bc7-754a-4f69-9348-75603e2257a4">IOpcSignatureReference</a> interface pointer at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7a260c3-cfe5-4dcb-9628-7cf7fdf382de">MoveNext</a>
</td>
<td align="left" width="63%">
Moves the current position of the enumerator to the next <a href="https://msdn.microsoft.com/2ce40bc7-754a-4f69-9348-75603e2257a4">IOpcSignatureReference</a> interface pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ff697a4-45fe-46cd-8d36-96bafcb32aa1">MovePrevious</a>
</td>
<td align="left" width="63%">
Moves the current position of the enumerator to the previous <a href="https://msdn.microsoft.com/2ce40bc7-754a-4f69-9348-75603e2257a4">IOpcSignatureReference</a>
    interface pointer.

</td>
</tr>
</table> 


## -remarks




  		When an enumerator is created, the current position precedes the first pointer. To set the current position to the first pointer of the enumerator, call the  <a href="https://msdn.microsoft.com/b7a260c3-cfe5-4dcb-9628-7cf7fdf382de">MoveNext</a>
          method after creating the enumerator.

Changes to the set will invalidate the enumerator, and all subsequent calls to it will fail.

To get an <b>IOpcSignatureReferenceEnumerator</b> interface pointer, call the <a href="https://msdn.microsoft.com/a4c39119-7317-408c-9173-efd6d449002e">IOpcSignatureReferenceSet::GetEnumerator</a> or <a href="https://msdn.microsoft.com/8cc5ae5d-faef-451d-8ad8-db4b8b5c0e22">IOpcDigitalSignature::GetCustomReferenceEnumerator</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/cfa38ef6-9d96-4577-a3bf-518784d19ad8">IOpcDigitalSignature</a>



<a href="https://msdn.microsoft.com/7955ac86-de6e-4911-a107-a1617c14e685">IOpcSignatureReferenceSet</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

