---
UID: NF:msopc.IOpcSigningOptions.GetSignaturePartName
title: IOpcSigningOptions::GetSignaturePartName (msopc.h)
author: windows-sdk-content
description: Gets the part name of the signature part where the signature markup will be stored.
old-location: opc\iopcsigningoptions_getsignaturepartname.htm
tech.root: OPC
ms.assetid: 09481639-eea1-4203-932f-e97558408b42
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSignaturePartName, GetSignaturePartName method [Open Packaging Conventions], GetSignaturePartName method [Open Packaging Conventions],IOpcSigningOptions interface, IOpcSigningOptions interface [Open Packaging Conventions],GetSignaturePartName method, IOpcSigningOptions.GetSignaturePartName, IOpcSigningOptions::GetSignaturePartName, msopc/IOpcSigningOptions::GetSignaturePartName, opc.iopcsigningoptions_getsignaturepartname
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
 - IOpcSigningOptions.GetSignaturePartName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcSigningOptions::GetSignaturePartName


## -description


Gets the part name of the signature part where the signature markup will be stored.


## -parameters




### -param signaturePartName [out, retval]

An <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface pointer that represents the part name of the part where the signature markup is stored,  or <b>NULL</b> if the part name  has not been set by a call to  the <a href="https://msdn.microsoft.com/36d69a11-bfc3-4f0a-a681-4e138751990d">SetSignaturePartName</a> method.


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
The <i>signaturePartName</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



To set the part name of the signature part that stores the signature markup, call  the <a href="https://msdn.microsoft.com/36d69a11-bfc3-4f0a-a681-4e138751990d">IOpcSigningOptions::SetSignaturePartName</a> method.

To access the signature part name after the signature is generated, call the <a href="https://msdn.microsoft.com/0a7f9413-d44d-4d3d-bb4e-01ef14ee7a1c">IOpcDigitalSignature::GetSignaturePartName</a> method.

The signature part that stores signature markup is specific to the signature.


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
 

 

