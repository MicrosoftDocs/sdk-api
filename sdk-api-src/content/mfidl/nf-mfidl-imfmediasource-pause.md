---
UID: NF:mfidl.IMFMediaSource.Pause
title: IMFMediaSource::Pause
author: windows-driver-content
description: Pauses all active streams in the media source.
old-location: mf\imfmediasource_pause.htm
old-project: medfound
ms.assetid: 113b3dc7-918e-427e-aa70-cf474b951c6d
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: 113b3dc7-918e-427e-aa70-cf474b951c6d, IMFMediaSource interface [Media Foundation],Pause method, IMFMediaSource.Pause, IMFMediaSource::Pause, Pause, Pause method [Media Foundation], Pause method [Media Foundation],IMFMediaSource interface, mf.imfmediasource_pause, mfidl/IMFMediaSource::Pause
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFMediaSource.Pause
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaSource::Pause


## -description



Pauses all active streams in the media source.




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
<dt><b>MF_E_INVALID_STATE_TRANSITION</b></dt>
</dl>
</td>
<td width="60%">
Invalid state transition. The media source must be in the started state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The media source's <a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">Shutdown</a> method has been called.

</td>
</tr>
</table>
 




## -remarks



This method is asynchronous. When the operation completes, the media source sends and <a href="https://msdn.microsoft.com/cca03d60-47ae-4a11-b29d-81d749e24df9">MESourcePaused</a> event, and every active stream sends an <a href="https://msdn.microsoft.com/8fafb9a1-95a4-44b6-acd6-fb007d515915">MEStreamPaused</a> event. If the method returns a failure code, no events are raised.

The media source must be in the started state. The method fails if the media source is paused or stopped.

While the source is paused, calls to <a href="https://msdn.microsoft.com/3838167b-5774-47f5-9b8d-2882eaa97167">IMFMediaStream::RequestSample</a> succeed, but the streams will not deliver any samples until after the source is started again. Note that the source's event queue is not serialized with the stream event queues, so the client might receive some samples after the <a href="https://msdn.microsoft.com/cca03d60-47ae-4a11-b29d-81d749e24df9">MESourcePaused</a> event, due to multi-threading issues. But the client will not receive any samples from a stream after the <a href="https://msdn.microsoft.com/8fafb9a1-95a4-44b6-acd6-fb007d515915">MEStreamPaused</a> event.

Not every media source can pause. If a media source can pause, the <a href="https://msdn.microsoft.com/cb5d54cd-58a3-4903-b22e-8207f90dbbc0">IMFMediaSource::GetCharacteristics</a> method returns the MFMEDIASOURCE_CAN_PAUSE flag.




## -see-also




<a href="https://msdn.microsoft.com/8b579f61-6fea-4b20-a051-7633fc01fa05">IMFMediaSource</a>



<a href="https://msdn.microsoft.com/65132e7d-22f6-4209-bc58-f5ea86ebd514">Media Sources</a>
 

 

