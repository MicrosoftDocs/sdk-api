---
UID: NF:msopc.IOpcDigitalSignatureManager.CreateSigningOptions
title: IOpcDigitalSignatureManager::CreateSigningOptions
author: windows-sdk-content
description: Creates an IOpcSigningOptions interface pointer.
old-location: opc\iopcdigitalsignaturemanager_createsigningoptions.htm
old-project: OPC
ms.assetid: c58f9730-b2c2-40cd-8aae-03fbd09f8c76
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CreateSigningOptions, CreateSigningOptions method [Open Packaging Conventions], CreateSigningOptions method [Open Packaging Conventions],IOpcDigitalSignatureManager interface, IOpcDigitalSignatureManager interface [Open Packaging Conventions],CreateSigningOptions method, IOpcDigitalSignatureManager.CreateSigningOptions, IOpcDigitalSignatureManager::CreateSigningOptions, msopc/IOpcDigitalSignatureManager::CreateSigningOptions, opc.iopcdigitalsignaturemanager_createsigningoptions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msopc.h
req.include-header: 
req.redist: 
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
 - IOpcDigitalSignatureManager.CreateSigningOptions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcDigitalSignatureManager::CreateSigningOptions


## -description


Creates an <a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a> interface pointer.


## -parameters




### -param signingOptions [out, retval]

A pointer to an <a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a> interface pointer.


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
The <i>signingOptions</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method creates an <a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a> interface pointer that is required to set the properties of a signature to be generated

To generate a signature, call the <a href="https://msdn.microsoft.com/5d40cae4-67d5-40a6-bd63-cf6243a703eb">IOpcDigitalSignatureManager::Sign</a> method with the <i>signingOptions</i> parameter value set to an <a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a> interface pointer that is retrieved by the <b>CreateSigningOptions</b> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/13e8a7b9-1d25-421b-bc81-adc495e6d9c7">IOpcDigitalSignatureManager</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

