---
UID: NF:msopc.IOpcSigningOptions.SetSignatureId
title: IOpcSigningOptions::SetSignatureId
author: windows-sdk-content
description: Sets the value of the Id attribute of the Signature element.
old-location: opc\iopcsigningoptions_setsignatureid.htm
old-project: OPC
ms.assetid: c723d6e8-6af3-41a2-b6dd-d26897495965
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IOpcSigningOptions interface [Open Packaging Conventions],SetSignatureId method, IOpcSigningOptions.SetSignatureId, IOpcSigningOptions::SetSignatureId, SetSignatureId, SetSignatureId method [Open Packaging Conventions], SetSignatureId method [Open Packaging Conventions],IOpcSigningOptions interface, msopc/IOpcSigningOptions::SetSignatureId, opc.iopcsigningoptions_setsignatureid
ms.prod: windows
ms.technology: windows-sdk
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
 - IOpcSigningOptions.SetSignatureId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcSigningOptions::SetSignatureId


## -description


Sets the value of the <b>Id</b> attribute of the <b>Signature</b> element.


## -parameters




### -param signatureId [in]

The value of the <b>Id</b> attribute.


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



The <b>Id</b> attribute of the <b>Signature</b> element is optional. If this method is not called, the <b>Signature</b> element will not have the <b>Id</b> attribute.

To access the Id before the signature is generated, call the <a href="https://msdn.microsoft.com/b81b49de-aaee-4224-9f5c-554b51f10cfa">IOpcSigningOptions::GetSignatureId</a>.  To access the signature Id after the signature is generated, call the <a href="https://msdn.microsoft.com/20eea0ff-dff1-4f95-aaf7-00e5a36503f1">IOpcDigitalSignature::GetSignatureId</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



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
 

 

