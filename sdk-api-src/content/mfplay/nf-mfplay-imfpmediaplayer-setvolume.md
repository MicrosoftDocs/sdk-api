---
UID: NF:mfplay.IMFPMediaPlayer.SetVolume
title: IMFPMediaPlayer::SetVolume
author: windows-driver-content
description: Sets the audio volume.
old-location: mf\imfpmediaplayer_setvolume.htm
old-project: medfound
ms.assetid: feee2812-7c7e-4c27-86be-8f7316854222
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IMFPMediaPlayer interface [Media Foundation],SetVolume method, IMFPMediaPlayer.SetVolume, IMFPMediaPlayer::SetVolume, SetVolume, SetVolume method [Media Foundation], SetVolume method [Media Foundation],IMFPMediaPlayer interface, mf.imfpmediaplayer_setvolume, mfplay/IMFPMediaPlayer::SetVolume
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
req.typenames: "_MFP_MEDIAITEM_CHARACTERISTICS"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfplay.h
api_name:
-	IMFPMediaPlayer.SetVolume
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPMediaPlayer::SetVolume


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Sets the audio volume.


## -parameters




### -param flVolume [in]

The volume level. Volume is expressed as an attenuation level, where 0.0 indicates silence and 1.0 indicates full volume (no attenuation).


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
<dt><b>MF_E_OUT_OF_RANGE</b></dt>
</dl>
</td>
<td width="60%">
The <i>flVolume</i> parameter is invalid.

</td>
</tr>
</table>
 




## -remarks



If you call this method before playback starts, the setting is applied after playback starts.

This method does not change the master volume level for the player's audio session. Instead, it adjusts the per-channel volume levels for audio stream(s) that belong to the current media item. Other streams in the audio session are not affected. For more information, see <a href="https://msdn.microsoft.com/4cf3dd0f-4c8a-4720-9eb3-d23352f3a85e">Managing the Audio Session</a>.




## -see-also




<a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

