---
UID: NF:mfplay.IMFPMediaPlayer.SetRate
title: IMFPMediaPlayer::SetRate
author: windows-sdk-content
description: Sets the playback rate.
old-location: mf\imfpmediaplayer_setrate.htm
old-project: medfound
ms.assetid: 7e9d4a0d-b61f-47d9-af47-d8a07cd728f6
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFPMediaPlayer interface [Media Foundation],SetRate method, IMFPMediaPlayer.SetRate, IMFPMediaPlayer::SetRate, SetRate, SetRate method [Media Foundation], SetRate method [Media Foundation],IMFPMediaPlayer interface, mf.imfpmediaplayer_setrate, mfplay/IMFPMediaPlayer::SetRate
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: "_MFP_MEDIAITEM_CHARACTERISTICS"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplay.h
api_name:
 - IMFPMediaPlayer.SetRate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPMediaPlayer::SetRate


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Sets the playback rate.


## -parameters




### -param flRate [in]

Playback rate. The playback rate is expressed as a ratio of the current rate to the normal rate. For example, <b>1.0</b> indicates normal playback speed, <b>0.5</b> indicates half speed, and <b>2.0</b> indicates twice speed. Positive values indicate forward playback, and negative values indicate reverse playback.


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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_OUT_OF_RANGE</b></b></dt>
</dl>
</td>
<td width="60%">
The <i>flRate</i> parameter is zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_SHUTDOWN</b></b></dt>
</dl>
</td>
<td width="60%">
The object's <a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">Shutdown</a> method was called.

</td>
</tr>
</table>
 




## -remarks



This method completes asynchronously.  When the operation completes, the application's <a href="https://msdn.microsoft.com/2a80a9d0-83ee-4bb0-ab2c-0f68367f3bf8">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a> callback method is invoked. The event type is <b>MFP_EVENT_TYPE_RATE_SET</b>.

The method sets the nearest supported rate, which will depend on the underlying media source. For example, if <i>flRate</i> is 50 and the source's maximum rate is 8× normal rate, the method will set the rate to 8.0.  The actual rate is indicated in the event data for the <b>MFP_EVENT_TYPE_RATE_SET</b> event.

To find the range of supported rates, call <a href="https://msdn.microsoft.com/e0e738e4-b8e4-41da-8b74-74ce06f17274">IMFPMediaPlayer::GetSupportedRates</a>.

This method does not support playback rates of zero, although Media Foundation defines a meaning for zero rates in some other contexts.

The new rate applies only to the current media item. Setting a new media item resets the playback rate to 1.0.




## -see-also




<a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

