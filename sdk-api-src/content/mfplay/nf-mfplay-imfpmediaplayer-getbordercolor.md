---
UID: NF:mfplay.IMFPMediaPlayer.GetBorderColor
title: IMFPMediaPlayer::GetBorderColor method
author: windows-driver-content
description: Gets the current color of the video border.
old-location: mf\imfpmediaplayer_getbordercolor.htm
old-project: medfound
ms.assetid: a07bacbd-3d45-4733-a506-3c54ec10b634
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetBorderColor method [Media Foundation], GetBorderColor method [Media Foundation], IMFPMediaPlayer interface, GetBorderColor,IMFPMediaPlayer.GetBorderColor, IMFPMediaPlayer, IMFPMediaPlayer interface [Media Foundation], GetBorderColor method, IMFPMediaPlayer::GetBorderColor, mf.imfpmediaplayer_getbordercolor, mfplay/IMFPMediaPlayer::GetBorderColor
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
-	IMFPMediaPlayer.GetBorderColor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPMediaPlayer::GetBorderColor method


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
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
The object's <a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">Shutdown</a> method was called.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

