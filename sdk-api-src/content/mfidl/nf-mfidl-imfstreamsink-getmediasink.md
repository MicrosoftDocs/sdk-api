---
UID: NF:mfidl.IMFStreamSink.GetMediaSink
title: IMFStreamSink::GetMediaSink
author: windows-sdk-content
description: Retrieves the media sink that owns this stream sink.
old-location: mf\imfstreamsink_getmediasink.htm
old-project: medfound
ms.assetid: 799fb0ce-6a43-49c2-97cf-49c51d8f69cd
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: 799fb0ce-6a43-49c2-97cf-49c51d8f69cd, GetMediaSink, GetMediaSink method [Media Foundation], GetMediaSink method [Media Foundation],IMFStreamSink interface, IMFStreamSink interface [Media Foundation],GetMediaSink method, IMFStreamSink.GetMediaSink, IMFStreamSink::GetMediaSink, mf.imfstreamsink_getmediasink, mfidl/IMFStreamSink::GetMediaSink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFStreamSink.GetMediaSink
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFStreamSink::GetMediaSink


## -description



Retrieves the media sink that owns this stream sink.




## -parameters




### -param ppMediaSink [out]

Receives a pointer to the media sink's <a href="https://msdn.microsoft.com/103e6fd8-a18f-480a-8261-099623014659">IMFMediaSink</a> interface. The caller must release the interface.


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
The media sink's <a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">Shutdown</a> method has been called.

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
 




## -see-also




<a href="https://msdn.microsoft.com/fe403cab-b901-4c8e-a23c-788ee65c4689">IMFStreamSink</a>



<a href="https://msdn.microsoft.com/a0fbce1b-0a16-4449-9eca-906fd9056a1c">Media Sinks</a>
 

 

