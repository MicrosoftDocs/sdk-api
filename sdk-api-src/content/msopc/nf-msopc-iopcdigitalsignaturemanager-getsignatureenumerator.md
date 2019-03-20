---
UID: NF:msopc.IOpcDigitalSignatureManager.GetSignatureEnumerator
title: IOpcDigitalSignatureManager::GetSignatureEnumerator (msopc.h)
author: windows-sdk-content
description: Gets an enumerator of IOpcDigitalSignature interface pointers, which represent package signatures.
old-location: opc\iopcdigitalsignaturemanager_getsignatureenumerator.htm
tech.root: OPC
ms.assetid: 44906f03-806f-400c-a7f3-0da5c330e1ff
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSignatureEnumerator, GetSignatureEnumerator method [Open Packaging Conventions], GetSignatureEnumerator method [Open Packaging Conventions],IOpcDigitalSignatureManager interface, IOpcDigitalSignatureManager interface [Open Packaging Conventions],GetSignatureEnumerator method, IOpcDigitalSignatureManager.GetSignatureEnumerator, IOpcDigitalSignatureManager::GetSignatureEnumerator, msopc/IOpcDigitalSignatureManager::GetSignatureEnumerator, opc.iopcdigitalsignaturemanager_getsignatureenumerator
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
 - IOpcDigitalSignatureManager.GetSignatureEnumerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcDigitalSignatureManager::GetSignatureEnumerator


## -description


Gets an enumerator of <a href="https://msdn.microsoft.com/cfa38ef6-9d96-4577-a3bf-518784d19ad8">IOpcDigitalSignature</a> interface pointers, which represent package signatures.


## -parameters




### -param signatureEnumerator [out, retval]

A pointer to  an enumerator of <a href="https://msdn.microsoft.com/cfa38ef6-9d96-4577-a3bf-518784d19ad8">IOpcDigitalSignature</a> interface pointers, which represent package signatures.


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
The <i>signatureEnumerator</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/73fd0e47-7503-470d-b649-e4b2ba492bf1">IOpcDigitalSignatureEnumerator</a>



<a href="https://msdn.microsoft.com/13e8a7b9-1d25-421b-bc81-adc495e6d9c7">IOpcDigitalSignatureManager</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

