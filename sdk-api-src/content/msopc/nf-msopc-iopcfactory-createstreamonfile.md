---
UID: NF:msopc.IOpcFactory.CreateStreamOnFile
title: IOpcFactory::CreateStreamOnFile
author: windows-sdk-content
description: Creates a stream over a file.
old-location: opc\iopcfactory_createstreamonfile.htm
old-project: OPC
ms.assetid: d41bb51d-127c-4b24-8c93-4224404e0b2d
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CreateStreamOnFile, CreateStreamOnFile method [Open Packaging Conventions], CreateStreamOnFile method [Open Packaging Conventions],IOpcFactory interface, IOpcFactory interface [Open Packaging Conventions],CreateStreamOnFile method, IOpcFactory.CreateStreamOnFile, IOpcFactory::CreateStreamOnFile, msopc/IOpcFactory::CreateStreamOnFile, opc.iopcfactory_createstreamonfile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msopc.h
req.include-header: 
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msopc.h
api_name:
 - IOpcFactory.CreateStreamOnFile
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcFactory::CreateStreamOnFile


## -description


Creates a stream over a file. This method is a simplified wrapper for a call to the <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function. <b>CreateFile</b> parameters that are not exposed through this method use their default values. For more information, see <b>CreateFile</b>.


## -parameters




### -param filename [in]

The name of the file over which the stream is created.


### -param ioMode [in]

The value that describes the read/write status of the stream to be created.


### -param securityAttributes [in]

For information about the <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> structure in this parameter, see the <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function.


### -param dwFlagsAndAttributes [in]

The settings and attributes of the file. For most files, <b>FILE_ATTRIBUTE_NORMAL</b> can be used.

For more information about this parameter, see <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>.


### -param stream [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface of the stream.


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
The value passed in the <i>ioMode</i> parameter is not a valid <a href="https://msdn.microsoft.com/cf72ddcf-5472-451f-bfa8-94f549dc9246">OPC_STREAM_IO_MODE</a> enumeration value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
At least one of the <i>filename</i> and <i>stream</i> parameters is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>CreateFile</b> function error</b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from the <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function. 

</td>
</tr>
</table>
 




## -remarks



Do not use a stream to serialize package data when the same stream is being used to deserialize a package, because the attempt may result in undefined behavior.

For information about using this method when loading or saving a package, see the <a href="https://msdn.microsoft.com/d9651962-71a0-4cd1-ab26-00bc0fa15b62">Loading a Package</a> or  <a href="https://msdn.microsoft.com/120436c8-7a12-4d48-be84-a02bbb672c7f">Saving a Package</a> programming task. 

<h3><a id="Support_on__Previous_Windows_Versions"></a><a id="support_on__previous_windows_versions"></a><a id="SUPPORT_ON__PREVIOUS_WINDOWS_VERSIONS"></a>Support on  Previous Windows Versions</h3>
The behavior and performance of this method is the same on all supported Windows versions. For more information, see <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>, and <a href="https://msdn.microsoft.com/661f88f9-e5ba-412d-8cb4-f3f186568b74">Platform Update for Windows Vista</a>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/0a265a0a-c109-4afc-a0ad-d3ee31757aa1">IOpcFactory</a>



<a href="https://msdn.microsoft.com/d9651962-71a0-4cd1-ab26-00bc0fa15b62">Loading a Package</a>



<a href="https://msdn.microsoft.com/cf72ddcf-5472-451f-bfa8-94f549dc9246">OPC_STREAM_IO_MODE</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>



<a href="https://msdn.microsoft.com/95da581d-3d30-4cd7-bd20-f44bf505ac0a">Parts Overview</a>



<a href="https://msdn.microsoft.com/661f88f9-e5ba-412d-8cb4-f3f186568b74">Platform Update for Windows Vista</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=143950">RFC 3986: URI Generic Syntax</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/120436c8-7a12-4d48-be84-a02bbb672c7f">Saving a Package</a>
 

 

