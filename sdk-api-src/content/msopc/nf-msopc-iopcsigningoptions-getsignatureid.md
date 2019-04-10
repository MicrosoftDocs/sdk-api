---
UID: NF:msopc.IOpcSigningOptions.GetSignatureId
title: IOpcSigningOptions::GetSignatureId (msopc.h)
author: windows-sdk-content
description: Gets the value of the Id attribute from the Signature element.
old-location: opc\iopcsigningoptions_getsignatureid.htm
tech.root: OPC
ms.assetid: b81b49de-aaee-4224-9f5c-554b51f10cfa
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSignatureId, GetSignatureId method [Open Packaging Conventions], GetSignatureId method [Open Packaging Conventions],IOpcSigningOptions interface, IOpcSigningOptions interface [Open Packaging Conventions],GetSignatureId method, IOpcSigningOptions.GetSignatureId, IOpcSigningOptions::GetSignatureId, msopc/IOpcSigningOptions::GetSignatureId, opc.iopcsigningoptions_getsignatureid
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
 - IOpcSigningOptions.GetSignatureId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcSigningOptions::GetSignatureId


## -description


Gets the value of the <b>Id</b> attribute from the <b>Signature</b> element.


## -parameters




### -param signatureId [out, retval]

A pointer to the value of the <b>Id</b> attribute, or the empty string "" if there is no <b>Id</b>.


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
The <i>signatureId</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method allocates memory used by the string returned in <i>signatureId</i>.  If the method succeeds, call the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function to free the memory.

The <b>Id</b> attribute of the <b>Signature</b> element is optional.

To set the signature Id, call  the <a href="https://msdn.microsoft.com/c723d6e8-6af3-41a2-b6dd-d26897495965">IOpcSigningOptions::SetSignatureId</a> method.

To access the Id before the signature is generated, call the <b>IOpcSigningOptions::GetSignatureId</b>.  To access the signature Id after the signature is generated, call the <a href="https://msdn.microsoft.com/20eea0ff-dff1-4f95-aaf7-00e5a36503f1">IOpcDigitalSignature::GetSignatureId</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/cfa38ef6-9d96-4577-a3bf-518784d19ad8">IOpcDigitalSignature</a>



<a href="https://msdn.microsoft.com/13e8a7b9-1d25-421b-bc81-adc495e6d9c7">IOpcDigitalSignatureManager</a>



<a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

