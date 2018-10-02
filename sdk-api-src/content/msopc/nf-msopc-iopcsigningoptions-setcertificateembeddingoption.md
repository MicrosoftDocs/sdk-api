---
UID: NF:msopc.IOpcSigningOptions.SetCertificateEmbeddingOption
title: IOpcSigningOptions::SetCertificateEmbeddingOption
author: windows-sdk-content
description: Set the storage location of the certificate to be used for the signature.
old-location: opc\iopcsigningoptions_setcertificateembeddingoption.htm
tech.root: OPC
ms.assetid: afae4b98-c05f-4fa3-bb1e-f9f43ee86e64
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IOpcSigningOptions interface [Open Packaging Conventions],SetCertificateEmbeddingOption method, IOpcSigningOptions.SetCertificateEmbeddingOption, IOpcSigningOptions::SetCertificateEmbeddingOption, SetCertificateEmbeddingOption, SetCertificateEmbeddingOption method [Open Packaging Conventions], SetCertificateEmbeddingOption method [Open Packaging Conventions],IOpcSigningOptions interface, msopc/IOpcSigningOptions::SetCertificateEmbeddingOption, opc.iopcsigningoptions_setcertificateembeddingoption
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
 - IOpcSigningOptions.SetCertificateEmbeddingOption
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcSigningOptions::SetCertificateEmbeddingOption


## -description


Set the storage location of the certificate to be used for the signature.


## -parameters




### -param embeddingOption [in]

The <a href="https://msdn.microsoft.com/4292a53b-33a2-431c-806a-7e8c96ecce40">OPC_CERTIFICATE_EMBEDDING_OPTION</a> value that describes the location of the certificate.


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
The <i>embeddingOption</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method changes the location of the certificate from the default location, <b>OPC_CERTIFICATE_IN_CERTIFICATE_PART</b>, to a location that is specified by the caller.

To access the value that describes the certificate location, call the <a href="https://msdn.microsoft.com/86f83829-0507-4918-ae7f-71738f985068">IOpcSigningOptions::GetCertificateEmbeddingOption</a> method.


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
 

 

