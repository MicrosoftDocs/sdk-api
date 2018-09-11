---
UID: NF:msopc.IOpcDigitalSignatureManager.GetSignatureOriginPartName
title: IOpcDigitalSignatureManager::GetSignatureOriginPartName
author: windows-sdk-content
description: Gets an IOpcPartUri interface pointer that represents the part name of the Digital Signature Origin part.
old-location: opc\iopcdigitalsignaturemanager_getsignatureoriginpartname.htm
tech.root: OPC
ms.assetid: 958cf2e7-0956-489a-904f-01ec00af48d1
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetSignatureOriginPartName, GetSignatureOriginPartName method [Open Packaging Conventions], GetSignatureOriginPartName method [Open Packaging Conventions],IOpcDigitalSignatureManager interface, IOpcDigitalSignatureManager interface [Open Packaging Conventions],GetSignatureOriginPartName method, IOpcDigitalSignatureManager.GetSignatureOriginPartName, IOpcDigitalSignatureManager::GetSignatureOriginPartName, msopc/IOpcDigitalSignatureManager::GetSignatureOriginPartName, opc.iopcdigitalsignaturemanager_getsignatureoriginpartname
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
 - IOpcDigitalSignatureManager.GetSignatureOriginPartName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcDigitalSignatureManager::GetSignatureOriginPartName


## -description


Gets an <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface pointer that represents the part name of the Digital Signature Origin part.


## -parameters




### -param signatureOriginPartName [out, retval]

An <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface pointer, or <b>NULL</b> if the Digital Signature Origin part does not exist.


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
The <i>signatureOriginPartName</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



When using the APIs to generate a signature, set the Digital Signature Origin part name  by calling the <a href="https://msdn.microsoft.com/edf1590c-14a2-4887-a2df-20b5b4cb89a6">SetSignatureOriginPartName</a> method.


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
 

 

