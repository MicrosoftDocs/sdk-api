---
UID: NF:msopc.IOpcFactory.CreatePackageRootUri
title: IOpcFactory::CreatePackageRootUri
author: windows-sdk-content
description: Creates an OPC URI object that represents the root of a package.
old-location: opc\iopcfactory_createpackagerooturi.htm
old-project: OPC
ms.assetid: 5ec33743-d362-43d9-a66e-8223745b9664
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: CreatePackageRootUri, CreatePackageRootUri method [Open Packaging Conventions], CreatePackageRootUri method [Open Packaging Conventions],IOpcFactory interface, IOpcFactory interface [Open Packaging Conventions],CreatePackageRootUri method, IOpcFactory.CreatePackageRootUri, IOpcFactory::CreatePackageRootUri, msopc/IOpcFactory::CreatePackageRootUri, opc.iopcfactory_createpackagerooturi
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msopc.h
api_name:
-	IOpcFactory.CreatePackageRootUri
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcFactory::CreatePackageRootUri


## -description


Creates an OPC URI object that represents the root of  a package.


## -parameters




### -param rootUri [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/35ce7946-f7e7-4ac3-852f-e3fcca23d6d4">IOpcUri</a> interface of the OPC URI object that represents the URI of the root of a package.


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
The <i>rootUri</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The URI of the root of a package is always represented as "/".

<h3><a id="Support_on__Previous_Windows_Versions"></a><a id="support_on__previous_windows_versions"></a><a id="SUPPORT_ON__PREVIOUS_WINDOWS_VERSIONS"></a>Support on  Previous Windows Versions</h3>
The behavior and performance of this method is the same on all supported Windows versions. For more information, see <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>, and <a href="https://msdn.microsoft.com/661f88f9-e5ba-412d-8cb4-f3f186568b74">Platform Update for Windows Vista</a>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/0a265a0a-c109-4afc-a0ad-d3ee31757aa1">IOpcFactory</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>



<a href="https://msdn.microsoft.com/661f88f9-e5ba-412d-8cb4-f3f186568b74">Platform Update for Windows Vista</a>



<b>Reference</b>
 

 

