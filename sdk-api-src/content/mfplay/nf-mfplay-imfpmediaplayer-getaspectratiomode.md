---
UID: NF:mfplay.IMFPMediaPlayer.GetAspectRatioMode
title: IMFPMediaPlayer::GetAspectRatioMode
author: windows-sdk-content
description: Gets the current aspect-ratio correction mode. This mode controls whether the aspect ratio of the video is preserved during playback.
old-location: mf\imfpmediaplayer_getaspectratiomode.htm
old-project: medfound
ms.assetid: eaeb20d2-d547-4f88-a69f-7c3f46fe95ff
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetAspectRatioMode, GetAspectRatioMode method [Media Foundation], GetAspectRatioMode method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],GetAspectRatioMode method, IMFPMediaPlayer.GetAspectRatioMode, IMFPMediaPlayer::GetAspectRatioMode, mf.imfpmediaplayer_getaspectratiomode, mfplay/IMFPMediaPlayer::GetAspectRatioMode
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
 - IMFPMediaPlayer.GetAspectRatioMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPMediaPlayer::GetAspectRatioMode


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Gets the current aspect-ratio correction mode. This mode controls whether the aspect ratio of the video is preserved during playback.


## -parameters




### -param pdwAspectRatioMode [out]

Receives a bitwise <b>OR</b> of one or more flags from the <a href="https://msdn.microsoft.com/c0a34cff-f86f-4005-9320-5dadfdde5808">MFVideoAspectRatioMode</a> enumeration.


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
 

 

