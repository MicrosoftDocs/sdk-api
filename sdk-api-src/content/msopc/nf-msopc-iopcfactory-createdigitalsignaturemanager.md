---
UID: NF:msopc.IOpcFactory.CreateDigitalSignatureManager
title: IOpcFactory::CreateDigitalSignatureManager
author: windows-sdk-content
description: Creates a digital signature manager object for a package object.
old-location: opc\iopcfactory_createdigitalsignaturemanager.htm
tech.root: OPC
ms.assetid: ec0fe8b6-e968-4bcb-b468-bbf72ffce675
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateDigitalSignatureManager, CreateDigitalSignatureManager method [Open Packaging Conventions], CreateDigitalSignatureManager method [Open Packaging Conventions],IOpcFactory interface, IOpcFactory interface [Open Packaging Conventions],CreateDigitalSignatureManager method, IOpcFactory.CreateDigitalSignatureManager, IOpcFactory::CreateDigitalSignatureManager, msopc/IOpcFactory::CreateDigitalSignatureManager, opc.iopcfactory_createdigitalsignaturemanager
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
 - IOpcFactory.CreateDigitalSignatureManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcFactory::CreateDigitalSignatureManager


## -description


Creates a digital signature manager object for a package object.


## -parameters




### -param package [in]

A pointer to the <a href="https://msdn.microsoft.com/e7052dd2-c910-41d8-a58a-8f3e68e09dd0">IOpcPackage</a> interface of the package object to associate with the digital signature manager object.


### -param signatureManager [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/13e8a7b9-1d25-421b-bc81-adc495e6d9c7">IOpcDigitalSignatureManager</a> interface of the digital signature manager object that is created for use with the package object.

A digital signature manager object provides access to the Packaging API's digital signature interfaces and methods. These can be used to sign the package represented by the package object or to validate the signatures in a package that has already been signed.


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This method is not implemented for this version of Windows.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_DUPLICATE_SIGNATURE_ORIGIN_RELATIONSHIP</b></dt>
<dt>0x8051001B</dt>
</dl>
</td>
<td width="60%">
More than one relationship of the digital signature origin relationship type  exists, but only one such relationship is allowed.

For more information about this relationship type, see the <i>OPC</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_INVALID_SIGNATURE_ORIGIN_RELATIONSHIP</b></dt>
<dt>0x8051001C</dt>
</dl>
</td>
<td width="60%">
A package relationship of type digital signature origin is targeting a location that is external to the package. Digital Signature Origin parts must be located internally.

For more information about this relationship type, see the <i>OPC</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_MISSING_SIGNATURE_ORIGIN_PART</b></dt>
<dt>0x8051001F</dt>
</dl>
</td>
<td width="60%">
A relationship of type digital signature origin  was found, but the Digital Signature Origin part itself was not.

For more information about this relationship type, see the <i>OPC</i>.

</td>
</tr>
</table>
 




## -remarks



If a package is modified while <a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a> are being used to sign the package, signing may fail or result in an inconsistent signature or package.

<h3><a id="Support_on_Previous_Versions_of_Windows"></a><a id="support_on_previous_versions_of_windows"></a><a id="SUPPORT_ON_PREVIOUS_VERSIONS_OF_WINDOWS"></a>Support on Previous Versions of Windows</h3>
This method is not supported on versions of Windows prior to Windows 7. For more information, see <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>, and <a href="https://msdn.microsoft.com/661f88f9-e5ba-412d-8cb4-f3f186568b74">Platform Update for Windows Vista</a>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/0a265a0a-c109-4afc-a0ad-d3ee31757aa1">IOpcFactory</a>



<a href="https://msdn.microsoft.com/f4f337dc-85ba-4dd9-aba8-f81c0e29088e">Music Bundle Signature Sample</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>



<a href="https://msdn.microsoft.com/661f88f9-e5ba-412d-8cb4-f3f186568b74">Platform Update for Windows Vista</a>



<b>Reference</b>
 

 

