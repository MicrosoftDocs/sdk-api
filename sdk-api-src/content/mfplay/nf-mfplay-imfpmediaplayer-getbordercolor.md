---
UID: NF:mfplay.IMFPMediaPlayer.GetBorderColor
title: IMFPMediaPlayer::GetBorderColor (mfplay.h)
description: Gets the current color of the video border.
helpviewer_keywords: ["GetBorderColor","GetBorderColor method [Media Foundation]","GetBorderColor method [Media Foundation]","IMFPMediaPlayer interface","IMFPMediaPlayer interface [Media Foundation]","GetBorderColor method","IMFPMediaPlayer.GetBorderColor","IMFPMediaPlayer::GetBorderColor","mf.imfpmediaplayer_getbordercolor","mfplay/IMFPMediaPlayer::GetBorderColor"]
old-location: mf\imfpmediaplayer_getbordercolor.htm
tech.root: mf
ms.assetid: a07bacbd-3d45-4733-a506-3c54ec10b634
ms.date: 12/05/2018
ms.keywords: GetBorderColor, GetBorderColor method [Media Foundation], GetBorderColor method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],GetBorderColor method, IMFPMediaPlayer.GetBorderColor, IMFPMediaPlayer::GetBorderColor, mf.imfpmediaplayer_getbordercolor, mfplay/IMFPMediaPlayer::GetBorderColor
f1_keywords:
- mfplay/IMFPMediaPlayer.GetBorderColor
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
- IMFPMediaPlayer.GetBorderColor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPMediaPlayer::GetBorderColor


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Gets the current color of the video border. The border color is used to letterbox the video.


## -parameters




### -param pClr [out]

Receives the border color as a <b>COLORREF</b> value.


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
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The current media item does not contain video.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The object's <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown">Shutdown</a> method was called.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
 

 

