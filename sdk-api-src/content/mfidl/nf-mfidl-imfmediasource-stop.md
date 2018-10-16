---
UID: NF:mfidl.IMFMediaSource.Stop
title: IMFMediaSource::Stop
author: windows-sdk-content
description: Stops all active streams in the media source.
old-location: mf\imfmediasource_stop.htm
tech.root: medfound
ms.assetid: aa7af7a0-a6c2-4c9e-9f98-d36716679297
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: IMFMediaSource interface [Media Foundation],Stop method, IMFMediaSource.Stop, IMFMediaSource::Stop, Stop, Stop method [Media Foundation], Stop method [Media Foundation],IMFMediaSource interface, aa7af7a0-a6c2-4c9e-9f98-d36716679297, mf.imfmediasource_stop, mfidl/IMFMediaSource::Stop
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
 - IMFMediaSource.Stop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaSource::Stop


## -description



Stops all active streams in the media source.




## -parameters






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
The media source's <a href="https://msdn.microsoft.com/c7f890a8-74bd-4418-bb02-a3fee62dec6d">Shutdown</a> method has been called.

</td>
</tr>
</table>
 




## -remarks



This method is asynchronous. When the operation completes, the media source sends and <a href="https://msdn.microsoft.com/0eda9aa1-3aad-43ac-9d87-ab96e4ac319d">MESourceStopped</a> event, and every active stream sends an <a href="https://msdn.microsoft.com/80280820-b618-43d9-881e-6119dfa36e22">MEStreamStopped</a> event. If the method returns a failure code, no events are raised.

When a media source is stopped, its current position reverts to zero. After that, if the <a href="https://msdn.microsoft.com/0a5abafe-1525-4bda-946c-05a6145e57ee">Start</a> method is called with VT_EMPTY for the starting position, playback starts from the beginning of the presentation.

While the source is stopped, no streams produce data.




## -see-also




<a href="https://msdn.microsoft.com/8b579f61-6fea-4b20-a051-7633fc01fa05">IMFMediaSource</a>



<a href="https://msdn.microsoft.com/65132e7d-22f6-4209-bc58-f5ea86ebd514">Media Sources</a>
 

 

