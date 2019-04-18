---
UID: NF:msopc.IOpcDigitalSignature.GetTimeFormat
title: IOpcDigitalSignature::GetTimeFormat (msopc.h)
author: windows-sdk-content
description: Gets the format of the string returned by the GetSigningTime method.
old-location: opc\iopcdigitalsignature_gettimeformat.htm
tech.root: OPC
ms.assetid: df142c4d-27dc-4db3-9a37-78c5703c8119
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTimeFormat, GetTimeFormat method [Open Packaging Conventions], GetTimeFormat method [Open Packaging Conventions],IOpcDigitalSignature interface, IOpcDigitalSignature interface [Open Packaging Conventions],GetTimeFormat method, IOpcDigitalSignature.GetTimeFormat, IOpcDigitalSignature::GetTimeFormat, msopc/IOpcDigitalSignature::GetTimeFormat, opc.iopcdigitalsignature_gettimeformat
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
 - IOpcDigitalSignature.GetTimeFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOpcDigitalSignature::GetTimeFormat


## -description


Gets the format of the string returned by the <a href="https://msdn.microsoft.com/8054eba8-ca53-42e4-9105-ef7cf20637c1">GetSigningTime</a> method.


## -parameters




### -param timeFormat [out, retval]

An <a href="https://msdn.microsoft.com/9b8ff585-5795-48ce-b2fd-a49e3d34ccb9">OPC_SIGNATURE_TIME_FORMAT</a> value that describes the format of the string returned by <a href="https://msdn.microsoft.com/8054eba8-ca53-42e4-9105-ef7cf20637c1">GetSigningTime</a>.


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
The <i>timeFormat</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



To access a string that indicates the time at which the current package signature was generated, call the <a href="https://msdn.microsoft.com/8054eba8-ca53-42e4-9105-ef7cf20637c1">GetSigningTime</a> method.

To set the format of the signing time string before the signature is generated, call the <a href="https://msdn.microsoft.com/3f8c1dbe-6347-4013-bda6-5e08c9d6921d">IOpcSigningOptions::SetTimeFormat</a> method. To access the format before the signature is generated, call the <a href="https://msdn.microsoft.com/69394df9-5382-49eb-9aa2-0785dee10ac4">IOpcSigningOptions::GetTimeFormat</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



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
 

 

