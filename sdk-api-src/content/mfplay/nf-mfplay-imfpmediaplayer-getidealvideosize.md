---
UID: NF:mfplay.IMFPMediaPlayer.GetIdealVideoSize
title: IMFPMediaPlayer::GetIdealVideoSize
author: windows-sdk-content
description: Gets the range of video sizes that can be displayed without significantly degrading performance or image quality.
old-location: mf\imfpmediaplayer_getidealvideosize.htm
tech.root: medfound
ms.assetid: e6835852-10f0-4453-a22a-a567457bd7c5
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: GetIdealVideoSize, GetIdealVideoSize method [Media Foundation], GetIdealVideoSize method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],GetIdealVideoSize method, IMFPMediaPlayer.GetIdealVideoSize, IMFPMediaPlayer::GetIdealVideoSize, mf.imfpmediaplayer_getidealvideosize, mfplay/IMFPMediaPlayer::GetIdealVideoSize
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
 - IMFPMediaPlayer.GetIdealVideoSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMediaPlayer::GetIdealVideoSize


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Gets the range of video sizes that can be displayed without significantly degrading performance or image quality.


## -parameters




### -param pszMin [out]

Receives the minimum size that is preferable. This parameter can be <b>NULL</b>.


### -param pszMax [out]

Receives the maximum size that is preferable. This parameter can be <b>NULL</b>.


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



At least one parameter must be non-<b>NULL</b>. Sizes are given in pixels.




## -see-also




<a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

