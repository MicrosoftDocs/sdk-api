---
UID: NF:msopc.IOpcSignaturePartReferenceEnumerator.GetCurrent
title: IOpcSignaturePartReferenceEnumerator::GetCurrent method
author: windows-driver-content
description: Gets the IOpcSignaturePartReference interface pointer at the current position of the enumerator.
old-location: opc\iopcsignaturepartreferenceenumerator_getcurrent.htm
old-project: OPC
ms.assetid: ce5e90dd-9bf3-4632-a957-f468bf91415d
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GetCurrent method [Open Packaging Conventions], GetCurrent method [Open Packaging Conventions], IOpcSignaturePartReferenceEnumerator interface, GetCurrent,IOpcSignaturePartReferenceEnumerator.GetCurrent, IOpcSignaturePartReferenceEnumerator, IOpcSignaturePartReferenceEnumerator interface [Open Packaging Conventions], GetCurrent method, IOpcSignaturePartReferenceEnumerator::GetCurrent, msopc/IOpcSignaturePartReferenceEnumerator::GetCurrent, opc.iopcsignaturepartreferenceenumerator_getcurrent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OpcDigitalSignature.idl
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
-	IOpcSignaturePartReferenceEnumerator.GetCurrent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IOpcSignaturePartReferenceEnumerator::GetCurrent method


## -description


Gets the <a href="https://msdn.microsoft.com/b4bbf854-96b4-412b-a22d-c810423a3752">IOpcSignaturePartReference</a> interface pointer at the current position of the enumerator.


## -parameters




### -param partReference [out, retval]

An <a href="https://msdn.microsoft.com/b4bbf854-96b4-412b-a22d-c810423a3752">IOpcSignaturePartReference</a> interface pointer.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>partReference</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_ENUM_COLLECTION_CHANGED</b></dt>
<dt>0x80510050</dt>
</dl>
</td>
<td width="60%">
The enumerator is invalid because the underlying set has changed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_ENUM_INVALID_POSITION</b></dt>
<dt>0x80510053</dt>
</dl>
</td>
<td width="60%">
The enumerator cannot perform this operation from its current position.

</td>
</tr>
</table>
 




## -remarks




  		When an enumerator is created, the current position precedes the first pointer. To set the current position to the first pointer of the enumerator, call the  <a href="https://msdn.microsoft.com/2bf3c448-b09a-4102-bc3a-c65515d2a0a8">MoveNext</a>
          method after creating the enumerator.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/8a54debe-3ac6-471d-b5a5-c3512da4d079">IOpcSignaturePartReferenceEnumerator</a>



<a href="https://msdn.microsoft.com/c6f453e4-e0f5-4ecc-b622-6b30778ff719">IOpcSignaturePartReferenceSet</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

