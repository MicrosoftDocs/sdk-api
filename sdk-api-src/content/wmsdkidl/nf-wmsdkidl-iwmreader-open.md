---
UID: NF:wmsdkidl.IWMReader.Open
title: IWMReader::Open
author: windows-sdk-content
description: The Open method opens an ASF file for reading.
old-location: wmformat\iwmreader_open.htm
tech.root: wmformat
ms.assetid: ab5b7f9e-b647-4121-abb3-2c9deb1f50cc
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IWMReader interface [windows Media Format],Open method, IWMReader.Open, IWMReader::Open, IWMReaderOpen, Open, Open method [windows Media Format], Open method [windows Media Format],IWMReader interface, wmformat.iwmreader_open, wmsdkidl/IWMReader::Open
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMReader.Open
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReader::Open


## -description



The <b>Open</b> method opens an ASF file for reading.




## -parameters




### -param pwszURL [in]

Pointer to a wide-character <b>null</b>-terminated string containing the path and name of the file to be opened. This method accepts a path to a folder on a local machine, a path to a network share, or a uniform resource locator (URL).


### -param pCallback [in]

Pointer to the object that implements the <a href="https://msdn.microsoft.com/69b897a8-cc26-445d-9d41-b917b399fb14">IWMReaderCallback</a> interface.


### -param pvContext [in]

Generic pointer, for use by the application. This is passed to the application in calls to <b>OnStatus</b>.


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
The <i>pCallback</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough available memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
</table>
 




## -remarks



This method is asynchronous; it returns very quickly and sends a WMT_OPENED status notification to the application's <a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">IWMStatusCallback::OnStatus</a> method when the file is opened and ready for use.

Because the method returns before the file is opened, a return value of S_OK does not necessarily mean that the file has been opened successfully. To ascertain the success of the call, you must check the value of of the <i>hr</i> parameter of <b>OnStatus</b> when the WMT_OPENED notification is received.

If <i>hr</i> equals NS_E_NO_STREAM it means that the header is not yet available, and that a WMT_SOURCE_SWITCH event will be sent as soon as the header becomes available. No WMT_EOF will be sent before the WMT_SOURCE_SWITCH.

Applications that read files from behind a firewall will have better performance when opening files if the address is specified using the domain name server (DNS) name instead of the IP address.




## -see-also




<a href="https://msdn.microsoft.com/e995b707-d388-4ec3-b3c8-b111628c13d7">IWMReader Interface</a>



<a href="https://msdn.microsoft.com/3f320a0c-8586-4fc2-bd70-06ddda435cb5">IWMReader::Close</a>



<a href="https://msdn.microsoft.com/485844c6-7a84-4a0d-827d-060d8caef6cc">IWMReader::Start</a>



<a href="https://msdn.microsoft.com/781d1882-4b48-4415-9b3a-788207b42151">IWMReader::Stop</a>



<a href="https://msdn.microsoft.com/20822e1d-b367-4b03-9d8a-985427f0062d">IWMReaderAdvanced2::OpenStream</a>



<a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">IWMStatusCallback::OnStatus</a>
 

 

