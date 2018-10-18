---
UID: NF:mfplay.IMFPMediaPlayer.GetDuration
title: IMFPMediaPlayer::GetDuration
author: windows-sdk-content
description: Gets the playback duration of the current media item.
old-location: mf\imfpmediaplayer_getduration.htm
tech.root: medfound
ms.assetid: 7d201035-6946-4a46-bc66-b9e78006a04a
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: GetDuration, GetDuration method [Media Foundation], GetDuration method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],GetDuration method, IMFPMediaPlayer.GetDuration, IMFPMediaPlayer::GetDuration, MFP_POSITIONTYPE_100NS, mf.imfpmediaplayer_getduration, mfplay/IMFPMediaPlayer::GetDuration
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfplay.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - mfplay.h
api_name:
 - IMFPMediaPlayer.GetDuration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMediaPlayer::GetDuration


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Gets the playback duration of the current media item.


## -parameters




### -param guidPositionType [in]

Specifies the unit of time for the duration. The following value is defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MFP_POSITIONTYPE_100NS"></a><a id="mfp_positiontype_100ns"></a><dl>
<dt><b><b>MFP_POSITIONTYPE_100NS</b></b></dt>
</dl>
</td>
<td width="60%">
100-nanosecond units. 
               

The value returned in <i>pvDurationValue</i> is a <b>ULARGE_INTEGER</b>.

<ul>
<li>Variant type (<b>vt</b>): <b>VT_UI8</b></li>
<li>Variant member: <b>uhVal</b></li>
</ul>
</td>
</tr>
</table>
 


### -param pvDurationValue [out]

Pointer to a <b>PROPVARIANT</b> that receives the duration.


## -returns



This method can return one of these values.

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
<dt><b>MF_E_ATTRIBUTENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The media source does not have a duration. This error can occur with a live source, such as a video camera.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
There is no current media item.

</td>
</tr>
</table>
 




## -remarks



This method calculates the playback duration, taking into account the start and stop times for the media item. To set the start and stop times, call <a href="https://msdn.microsoft.com/8f0409a6-1911-47ee-ac65-68b87d6b1db5">IMFPMediaItem::SetStartStopPosition</a> on the media item. To get the actual duration of the underlying media file, regardless of start and stop times, call <a href="https://msdn.microsoft.com/831f023b-c06f-4099-9f4c-df38f3d1382f">IMFPMediaItem::GetDuration</a>.

For example, suppose that you load a 30-second audio file and set the start time equal to 2 seconds and stop time equal to 10 seconds. The <a href="https://msdn.microsoft.com/831f023b-c06f-4099-9f4c-df38f3d1382f">IMFPMediaItem::GetDuration</a> method will return 30 seconds, but the <b>IMFPMediaPlayer::GetDuration</b> method will return 8 seconds.




## -see-also




<a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

