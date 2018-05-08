---
UID: NF:msopc.IOpcDigitalSignature.GetSignaturePartReferenceEnumerator
title: IOpcDigitalSignature::GetSignaturePartReferenceEnumerator
author: windows-driver-content
description: Gets an enumerator of IOpcSignaturePartReference interface pointers, which represent references to parts that have been signed.
old-location: opc\iopcdigitalsignature_getsignaturepartreferenceenumerator.htm
old-project: OPC
ms.assetid: d8d1507e-b72f-4eb7-bd3d-4f4a26516c18
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GetSignaturePartReferenceEnumerator, GetSignaturePartReferenceEnumerator method [Open Packaging Conventions], GetSignaturePartReferenceEnumerator method [Open Packaging Conventions],IOpcDigitalSignature interface, IOpcDigitalSignature interface [Open Packaging Conventions],GetSignaturePartReferenceEnumerator method, IOpcDigitalSignature.GetSignaturePartReferenceEnumerator, IOpcDigitalSignature::GetSignaturePartReferenceEnumerator, msopc/IOpcDigitalSignature::GetSignaturePartReferenceEnumerator, opc.iopcdigitalsignature_getsignaturepartreferenceenumerator
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
-	IOpcDigitalSignature.GetSignaturePartReferenceEnumerator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IOpcDigitalSignature::GetSignaturePartReferenceEnumerator


## -description


Gets an enumerator of <a href="https://msdn.microsoft.com/b4bbf854-96b4-412b-a22d-c810423a3752">IOpcSignaturePartReference</a> interface pointers, which represent references to parts that have been signed.


## -parameters




### -param partReferenceEnumerator [out, retval]

A pointer to an enumerator of <a href="https://msdn.microsoft.com/b4bbf854-96b4-412b-a22d-c810423a3752">IOpcSignaturePartReference</a> interface pointers, which represent references to parts that have been signed.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
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
The <i>partReferenceEnumerator</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/cfa38ef6-9d96-4577-a3bf-518784d19ad8">IOpcDigitalSignature</a>



<a href="https://msdn.microsoft.com/8a54debe-3ac6-471d-b5a5-c3512da4d079">IOpcSignaturePartReferenceEnumerator</a>



<a href="https://msdn.microsoft.com/c6f453e4-e0f5-4ecc-b622-6b30778ff719">IOpcSignaturePartReferenceSet</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

