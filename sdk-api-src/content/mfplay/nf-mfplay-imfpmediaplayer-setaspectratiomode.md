---
UID: NF:mfplay.IMFPMediaPlayer.SetAspectRatioMode
title: IMFPMediaPlayer::SetAspectRatioMode
author: windows-sdk-content
description: Specifies whether the aspect ratio of the video is preserved during playback.
old-location: mf\imfpmediaplayer_setaspectratiomode.htm
tech.root: medfound
ms.assetid: b100a422-548f-4c38-afeb-4d4c1d9a9140
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IMFPMediaPlayer interface [Media Foundation],SetAspectRatioMode method, IMFPMediaPlayer.SetAspectRatioMode, IMFPMediaPlayer::SetAspectRatioMode, SetAspectRatioMode, SetAspectRatioMode method [Media Foundation], SetAspectRatioMode method [Media Foundation],IMFPMediaPlayer interface, mf.imfpmediaplayer_setaspectratiomode, mfplay/IMFPMediaPlayer::SetAspectRatioMode
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
 - IMFPMediaPlayer.SetAspectRatioMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMediaPlayer::SetAspectRatioMode


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Specifies whether the aspect ratio of the video is preserved during playback.


## -parameters




### -param dwAspectRatioMode [in]

Bitwise <b>OR</b> of one or more flags from the <a href="https://msdn.microsoft.com/c0a34cff-f86f-4005-9320-5dadfdde5808">MFVideoAspectRatioMode</a> enumeration.


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
<dt><b><b>MF_E_INVALIDREQUEST</b></b></dt>
</dl>
</td>
<td width="60%">
The current media item does not contain video.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_SHUTDOWN</b></b></dt>
</dl>
</td>
<td width="60%">
The object's <a href="https://msdn.microsoft.com/c56b07b5-f595-4933-9af6-868fc8938849">Shutdown</a> method was called.

</td>
</tr>
</table>
 




## -remarks



This method fails if no media item is currently set, or if the current media item does not contain video.

To set the aspect-ratio mode before playback starts, call this method inside your event handler for the <b>MFP_EVENT_TYPE_MEDIAITEM_SET</b> event. For more information, see <a href="https://msdn.microsoft.com/2a80a9d0-83ee-4bb0-ab2c-0f68367f3bf8">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a>.




## -see-also




<a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

