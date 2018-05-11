---
UID: NF:mfplay.IMFPMediaPlayer.RemoveEffect
title: IMFPMediaPlayer::RemoveEffect
author: windows-driver-content
description: Removes an effect that was added with the IMFPMediaPlayer::InsertEffect method.
old-location: mf\imfpmediaplayer_removeeffect.htm
old-project: medfound
ms.assetid: ca8507b9-c6c5-4e17-9c18-3ec1514de897
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IMFPMediaPlayer interface [Media Foundation],RemoveEffect method, IMFPMediaPlayer.RemoveEffect, IMFPMediaPlayer::RemoveEffect, RemoveEffect, RemoveEffect method [Media Foundation], RemoveEffect method [Media Foundation],IMFPMediaPlayer interface, mf.imfpmediaplayer_removeeffect, mfplay/IMFPMediaPlayer::RemoveEffect
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
-	IMFPMediaPlayer.RemoveEffect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPMediaPlayer::RemoveEffect


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Removes an effect that was added with the <a href="https://msdn.microsoft.com/2689ee46-5cfe-4616-850c-eb5aef340daa">IMFPMediaPlayer::InsertEffect</a> method.


## -parameters




### -param pEffect [in]

Pointer to the <b>IUnknown</b> interface of the effect object. Use the same pointer that you passed to the <a href="https://msdn.microsoft.com/2689ee46-5cfe-4616-850c-eb5aef340daa">InsertEffect</a> method.


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




<a href="https://msdn.microsoft.com/90f34bf3-899f-46e0-80c8-af83caa4835d">How to Add Audio or Video Effects</a>



<a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

