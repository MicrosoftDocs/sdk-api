---
UID: NN:msopc.IOpcSignaturePartReferenceEnumerator
title: IOpcSignaturePartReferenceEnumerator
author: windows-driver-content
description: A read-only enumerator of IOpcSignaturePartReference interface pointers.
old-location: opc\iopcsignaturepartreferenceenumerator.htm
old-project: OPC
ms.assetid: 8a54debe-3ac6-471d-b5a5-c3512da4d079
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IOpcSignaturePartReferenceEnumerator, IOpcSignaturePartReferenceEnumerator interface [Open Packaging Conventions], IOpcSignaturePartReferenceEnumerator interface [Open Packaging Conventions],described, msopc/IOpcSignaturePartReferenceEnumerator, opc.iopcsignaturepartreferenceenumerator
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
-	IOpcSignaturePartReferenceEnumerator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IOpcSignaturePartReferenceEnumerator interface


## -description


A read-only enumerator of <a href="https://msdn.microsoft.com/b4bbf854-96b4-412b-a22d-c810423a3752">IOpcSignaturePartReference</a> interface pointers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcSignaturePartReferenceEnumerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpcSignaturePartReferenceEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcSignaturePartReferenceEnumerator</b> interface has these methods.
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
Creates a copy of the current <b>IOpcSignaturePartReferenceEnumerator</b> interface pointer and all its descendants.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce5e90dd-9bf3-4632-a957-f468bf91415d">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/b4bbf854-96b4-412b-a22d-c810423a3752">IOpcSignaturePartReference</a> interface pointer at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2bf3c448-b09a-4102-bc3a-c65515d2a0a8">MoveNext</a>
</td>
<td align="left" width="63%">
Moves the current position of the enumerator to the next <a href="https://msdn.microsoft.com/b4bbf854-96b4-412b-a22d-c810423a3752">IOpcSignaturePartReference</a> interface pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/508c447e-dbbb-4e10-b9f7-c1d58ccf1895">MovePrevious</a>
</td>
<td align="left" width="63%">
Moves the current position of the enumerator to the previous <a href="https://msdn.microsoft.com/b4bbf854-96b4-412b-a22d-c810423a3752">IOpcSignaturePartReference</a> interface pointer.

</td>
</tr>
</table> 


## -remarks




  		When an enumerator is created, the current position precedes the first pointer. To set the current position to the first pointer of the enumerator, call the  <a href="https://msdn.microsoft.com/2bf3c448-b09a-4102-bc3a-c65515d2a0a8">MoveNext</a>
          method after creating the enumerator.

Changes to the set will invalidate the enumerator, and all subsequent calls to it will fail.

To get an <b>IOpcSignaturePartReferenceEnumerator</b> interface pointer, call the <a href="https://msdn.microsoft.com/5b345fe9-55b3-447c-9b5b-64ab292ab734">IOpcSignaturePartReferenceSet::GetEnumerator</a> or <a href="https://msdn.microsoft.com/d8d1507e-b72f-4eb7-bd3d-4f4a26516c18">IOpcDigitalSignature::GetSignaturePartReferenceEnumerator</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/cfa38ef6-9d96-4577-a3bf-518784d19ad8">IOpcDigitalSignature</a>



<a href="https://msdn.microsoft.com/c6f453e4-e0f5-4ecc-b622-6b30778ff719">IOpcSignaturePartReferenceSet</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

