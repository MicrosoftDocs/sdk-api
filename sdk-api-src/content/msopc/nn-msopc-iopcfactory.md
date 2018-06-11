---
UID: NN:msopc.IOpcFactory
title: IOpcFactory
author: windows-sdk-content
description: Creates Packaging API objects and provides support for saving and loading packages.
old-location: opc\iopcfactory.htm
old-project: OPC
ms.assetid: 0a265a0a-c109-4afc-a0ad-d3ee31757aa1
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: IOpcFactory, IOpcFactory interface [Open Packaging Conventions], IOpcFactory interface [Open Packaging Conventions],described, msopc/IOpcFactory, opc.iopcfactory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msopc.idl
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
 - IOpcFactory
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcFactory interface


## -description


Creates Packaging API objects and provides support for saving and loading packages.  Objects that are created by <b>IOpcFactory</b> interface methods provide support for creating, populating, modifying, and digitally signing packages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpcFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec0fe8b6-e968-4bcb-b468-bbf72ffce675">CreateDigitalSignatureManager</a>
</td>
<td align="left" width="63%">
Creates a digital signature manager object for a package object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9cd4ef3a-f890-40d5-a398-cb8f9746c380">CreatePackage</a>
</td>
<td align="left" width="63%">
Creates a package object that represents an empty package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ec33743-d362-43d9-a66e-8223745b9664">CreatePackageRootUri</a>
</td>
<td align="left" width="63%">
Creates an OPC URI object that represents the root of  a package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8634d166-767a-46a5-9001-5fca88bfa844">CreatePartUri</a>
</td>
<td align="left" width="63%">
Creates a part URI object that represents a part name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d41bb51d-127c-4b24-8c93-4224404e0b2d">CreateStreamOnFile</a>
</td>
<td align="left" width="63%">
Creates a stream over a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/227a2724-c2b3-4f12-8d30-1ff1eca59c83">ReadPackageFromStream</a>
</td>
<td align="left" width="63%">
              Deserializes package data from a stream  and creates a package object to represent the package being read.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b155700d-3037-4c6e-b2f2-bba39513d7d3">WritePackageToStream</a>
</td>
<td align="left" width="63%">
Serializes a package  that is represented by a package object. 

</td>
</tr>
</table> 


## -remarks



Do not use a stream to serialize package data when the same stream is being used to deserialize a package; attempting to do so may result in undefined behavior.

To use the Packaging API, the package must map to a ZIP archive as specified in the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>.

To create a factory that implements the <b>IOpcFactory</b> interface,  call the <a href="_com_CoCreateInstance">CoCreateInstance</a> function. This factory is not tied to any particular package or Packaging API object, and it can be used for the lifetime of the application. For example code that shows how to create a factory implementing  <b>IOpcFactory</b>, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.

<h3><a id="IOpcFactory_Support_on_Previous_Versions_of_Windows"></a><a id="iopcfactory_support_on_previous_versions_of_windows"></a><a id="IOPCFACTORY_SUPPORT_ON_PREVIOUS_VERSIONS_OF_WINDOWS"></a>IOpcFactory Support on Previous Versions of Windows</h3>
If an application attempts to an unsupported <b>IOpcFactory</b> method, the E_NOTIMPL error code will be returned. For more information, see <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>, and <a href="https://msdn.microsoft.com/661f88f9-e5ba-412d-8cb4-f3f186568b74">Platform Update for Windows Vista</a>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/13e8a7b9-1d25-421b-bc81-adc495e6d9c7">IOpcDigitalSignatureManager</a>



<a href="https://msdn.microsoft.com/e7052dd2-c910-41d8-a58a-8f3e68e09dd0">IOpcPackage</a>



<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/35ce7946-f7e7-4ac3-852f-e3fcca23d6d4">IOpcUri</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/661f88f9-e5ba-412d-8cb4-f3f186568b74">Platform Update for Windows Vista</a>



<b>Reference</b>
 

 

