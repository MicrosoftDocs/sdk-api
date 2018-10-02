---
UID: NF:msopc.IOpcDigitalSignature.GetSignatureValue
title: IOpcDigitalSignature::GetSignatureValue
author: windows-sdk-content
description: Gets the decoded value in the SignatureValue element of the signature markup.
old-location: opc\iopcdigitalsignature_getsignaturevalue.htm
tech.root: OPC
ms.assetid: c918d156-ad32-4a0c-83cc-dd37fe884744
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetSignatureValue, GetSignatureValue method [Open Packaging Conventions], GetSignatureValue method [Open Packaging Conventions],IOpcDigitalSignature interface, IOpcDigitalSignature interface [Open Packaging Conventions],GetSignatureValue method, IOpcDigitalSignature.GetSignatureValue, IOpcDigitalSignature::GetSignatureValue, msopc/IOpcDigitalSignature::GetSignatureValue, opc.iopcdigitalsignature_getsignaturevalue
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
 - IOpcDigitalSignature.GetSignatureValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcDigitalSignature::GetSignatureValue


## -description


Gets the decoded value in the <b>SignatureValue</b> element of the signature markup.


## -parameters




### -param signatureValue [out]

A pointer to a buffer that contains the decoded value in the <b>SignatureValue</b> element of the signature markup.


### -param count [out]

The size of the <i>signatureHashValue</i> buffer.


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
 At least one of the <i>signatureValue</i>, and <i>count</i> parameters is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method allocates memory used by the buffer returned in <i>signatureValue</i>.  If the method succeeds, call the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function to free the memory.

The <b>SignatureValue</b> element contains a base-64 encoded value that was computed by applying the signature method to the <b>SignedInfo</b> element of the signature markup. To get the signature method, call the <a href="https://msdn.microsoft.com/a4dfd99f-16d7-4bf1-9852-d6d1fd4a3f06">GetSignatureMethod</a> method.

When using the APIs to generate a signature, set the signature method by calling the <a href="https://msdn.microsoft.com/b567b09a-e688-4c02-8c01-983a307fd0e2">IOpcSigningOptions::SetSignatureMethod</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/cfa38ef6-9d96-4577-a3bf-518784d19ad8">IOpcDigitalSignature</a>



<a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

