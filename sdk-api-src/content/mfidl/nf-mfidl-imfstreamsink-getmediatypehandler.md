---
UID: NF:mfidl.IMFStreamSink.GetMediaTypeHandler
title: IMFStreamSink::GetMediaTypeHandler
author: windows-sdk-content
description: Retrieves the media type handler for the stream sink. You can use the media type handler to find which formats the stream supports, and to set the media type on the stream.
old-location: mf\imfstreamsink_getmediatypehandler.htm
tech.root: medfound
ms.assetid: 819d06b1-6b52-4496-bed8-a08b8f0b6153
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: 819d06b1-6b52-4496-bed8-a08b8f0b6153, GetMediaTypeHandler, GetMediaTypeHandler method [Media Foundation], GetMediaTypeHandler method [Media Foundation],IMFStreamSink interface, IMFStreamSink interface [Media Foundation],GetMediaTypeHandler method, IMFStreamSink.GetMediaTypeHandler, IMFStreamSink::GetMediaTypeHandler, mf.imfstreamsink_getmediatypehandler, mfidl/IMFStreamSink::GetMediaTypeHandler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFStreamSink.GetMediaTypeHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFStreamSink::GetMediaTypeHandler


## -description



Retrieves the media type handler for the stream sink. You can use the media type handler to find which formats the stream supports, and to set the media type on the stream.




## -parameters




### -param ppHandler [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/5b937bf7-4f86-4dc1-a4d5-7e724dcf5b36">IMFMediaTypeHandler</a> interface. The caller must release the interface.


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
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The media sink's <a href="https://msdn.microsoft.com/acda4e37-2dd0-4322-90fc-8f48d6842054">Shutdown</a> method has been called.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_STREAMSINK_REMOVED</b></dt>
</dl>
</td>
<td width="60%">
This stream was removed from the media sink and is no longer valid.

</td>
</tr>
</table>
 




## -remarks



If the stream sink currently does not support any media types, this method returns a media type handler that fails any calls to <a href="https://msdn.microsoft.com/b1676e40-81a2-4311-bba6-528bfa45a708">IMFMediaTypeHandler::GetCurrentMediaType</a> and <a href="https://msdn.microsoft.com/ea52defa-8b78-4f40-97ae-ed6a5ee4849e">IMFMediaTypeHandler::IsMediaTypeSupported</a>.




## -see-also




<a href="https://msdn.microsoft.com/fe403cab-b901-4c8e-a23c-788ee65c4689">IMFStreamSink</a>



<a href="https://msdn.microsoft.com/a0fbce1b-0a16-4449-9eca-906fd9056a1c">Media Sinks</a>
 

 

