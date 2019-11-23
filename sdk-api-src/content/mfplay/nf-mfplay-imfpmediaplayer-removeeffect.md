---
UID: NF:mfplay.IMFPMediaPlayer.RemoveEffect
title: IMFPMediaPlayer::RemoveEffect (mfplay.h)

description: Removes an effect that was added with the IMFPMediaPlayer::InsertEffect method.
old-location: mf\imfpmediaplayer_removeeffect.htm
tech.root: medfound
ms.assetid: ca8507b9-c6c5-4e17-9c18-3ec1514de897

ms.date: 12/05/2018
ms.keywords: IMFPMediaPlayer interface [Media Foundation],RemoveEffect method, IMFPMediaPlayer.RemoveEffect, IMFPMediaPlayer::RemoveEffect, RemoveEffect, RemoveEffect method [Media Foundation], RemoveEffect method [Media Foundation],IMFPMediaPlayer interface, mf.imfpmediaplayer_removeeffect, mfplay/IMFPMediaPlayer::RemoveEffect
ms.topic: method
f1_keywords: 
 - "mfplay/IMFPMediaPlayer.RemoveEffect"
dev_langs:
 - c++
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
 - IMFPMediaPlayer.RemoveEffect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPMediaPlayer::RemoveEffect


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Removes an effect that was added with the <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect">IMFPMediaPlayer::InsertEffect</a> method.


## -parameters




### -param pEffect [in]

Pointer to the <b>IUnknown</b> interface of the effect object. Use the same pointer that you passed to the <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect">InsertEffect</a> method.


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
<dt><b>MF_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The effect was not found.

</td>
</tr>
</table>
 




## -remarks



The change applies to the next media item that is set on the player. The effect is not removed from the current media item.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/how-to-add-audio-or-video-effects">How to Add Audio or Video Effects</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
 

 

