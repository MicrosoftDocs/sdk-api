---
UID: NF:msopc.IOpcDigitalSignatureManager.SetSignatureOriginPartName
title: IOpcDigitalSignatureManager::SetSignatureOriginPartName
author: windows-driver-content
description: Sets the part name of the Digital Signature Origin part to the name represented by a specified IOpcPartUri interface pointer.
old-location: opc\iopcdigitalsignaturemanager_setsignatureoriginpartname.htm
old-project: OPC
ms.assetid: edf1590c-14a2-4887-a2df-20b5b4cb89a6
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IOpcDigitalSignatureManager interface [Open Packaging Conventions],SetSignatureOriginPartName method, IOpcDigitalSignatureManager.SetSignatureOriginPartName, IOpcDigitalSignatureManager::SetSignatureOriginPartName, SetSignatureOriginPartName, SetSignatureOriginPartName method [Open Packaging Conventions], SetSignatureOriginPartName method [Open Packaging Conventions],IOpcDigitalSignatureManager interface, msopc/IOpcDigitalSignatureManager::SetSignatureOriginPartName, opc.iopcdigitalsignaturemanager_setsignatureoriginpartname
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
-	IOpcDigitalSignatureManager.SetSignatureOriginPartName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IOpcDigitalSignatureManager::SetSignatureOriginPartName


## -description


Sets the part name of the Digital Signature Origin part to the name represented by a specified <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface pointer.


## -parameters




### -param signatureOriginPartName [in]

A pointer to an <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface pointer that represents the desired part name for the Digital Signature Origin part.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code/value</th>
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
<dt><b>OPC_E_DS_SIGNATURE_ORIGIN_EXISTS</b></dt>
<dt>0x80510054</dt>
</dl>
</td>
<td width="60%">
A Digital Signature Origin part already exists in the package and cannot be renamed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DUPLICATE_PART</b></dt>
<dt>0x8051000B</dt>
</dl>
</td>
<td width="60%">
A part with the specified part name already exists in the current package.

</td>
</tr>
</table>
 




## -remarks



If the Digital Signature Origin part exists or if the part name that is in the <i>signatureOriginPartName</i> parameter is being used for another part, this method will fail.


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
 

 

