---
UID: NF:msopc.IOpcFactory.WritePackageToStream
title: IOpcFactory::WritePackageToStream
author: windows-driver-content
description: Serializes a package that is represented by a package object.
old-location: opc\iopcfactory_writepackagetostream.htm
old-project: OPC
ms.assetid: b155700d-3037-4c6e-b2f2-bba39513d7d3
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IOpcFactory interface [Open Packaging Conventions],WritePackageToStream method, IOpcFactory.WritePackageToStream, IOpcFactory::WritePackageToStream, WritePackageToStream, WritePackageToStream method [Open Packaging Conventions], WritePackageToStream method [Open Packaging Conventions],IOpcFactory interface, msopc/IOpcFactory::WritePackageToStream, opc.iopcfactory_writepackagetostream
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
req.typenames: OPC_SIGNATURE_TIME_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msopc.h
api_name:
-	IOpcFactory.WritePackageToStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcFactory::WritePackageToStream


## -description


Serializes a package  that is represented by a package object. 


## -parameters




### -param package [in]

A pointer to the <a href="https://msdn.microsoft.com/e7052dd2-c910-41d8-a58a-8f3e68e09dd0">IOpcPackage</a> interface  of the package object that contains data to be serialized.


### -param flags [in]

The value that describes the encoding method  used in serialization.


### -param stream [in]

A pointer to the <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface of the stream where the package object  data will be written.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value passed in the <i>flags</i> parameter is not a valid <a href="https://msdn.microsoft.com/12006b4a-98e1-4761-bce3-32b83b54a2cb">OPC_WRITE_FLAGS</a> enumeration value.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
At least one of the <i>stream</i> and <i>package</i> parameters is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>IStream</b> interface error</b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from the <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Package Consumption error</b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from the <a href="https://msdn.microsoft.com/0ad335ff-57da-4d4a-95c0-6b9b513a9698">Package Consumption Error Group</a>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Part URI error</b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from the <a href="https://msdn.microsoft.com/877447bb-d4e1-4277-b8ce-cb7a31a33fe0">Part URI Error Group</a>. 

</td>
</tr>
</table>
 




## -remarks



Do not use a stream to serialize package data when the same stream is being used to deserialize a package, because the attempt may result in undefined behavior.

For information about how to use this method to save a package that is represented as a package object, see the <a href="https://msdn.microsoft.com/120436c8-7a12-4d48-be84-a02bbb672c7f">Saving a Package</a> programming task. 

<h3><a id="Support_on_Previous_Versions_of_Windows"></a><a id="support_on_previous_versions_of_windows"></a><a id="SUPPORT_ON_PREVIOUS_VERSIONS_OF_WINDOWS"></a>Support on Previous Versions of Windows</h3>
This method is not supported on versions of Windows prior to Windows 7. For more information, see <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>, and <a href="https://msdn.microsoft.com/661f88f9-e5ba-412d-8cb4-f3f186568b74">Platform Update for Windows Vista</a>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/0a265a0a-c109-4afc-a0ad-d3ee31757aa1">IOpcFactory</a>



<a href="https://msdn.microsoft.com/12006b4a-98e1-4761-bce3-32b83b54a2cb">OPC_WRITE_FLAGS</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>



<a href="https://msdn.microsoft.com/661f88f9-e5ba-412d-8cb4-f3f186568b74">Platform Update for Windows Vista</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/120436c8-7a12-4d48-be84-a02bbb672c7f">Saving a Package</a>
 

 

