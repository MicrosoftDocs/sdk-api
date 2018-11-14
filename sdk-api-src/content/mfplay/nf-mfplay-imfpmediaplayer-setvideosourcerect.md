---
UID: NF:mfplay.IMFPMediaPlayer.SetVideoSourceRect
title: IMFPMediaPlayer::SetVideoSourceRect
author: windows-sdk-content
description: Sets the video source rectangle.
old-location: mf\imfpmediaplayer_setvideosourcerect.htm
tech.root: medfound
ms.assetid: c95d724f-40a9-43c5-b81a-8505eda516f7
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IMFPMediaPlayer interface [Media Foundation],SetVideoSourceRect method, IMFPMediaPlayer.SetVideoSourceRect, IMFPMediaPlayer::SetVideoSourceRect, SetVideoSourceRect, SetVideoSourceRect method [Media Foundation], SetVideoSourceRect method [Media Foundation],IMFPMediaPlayer interface, mf.imfpmediaplayer_setvideosourcerect, mfplay/IMFPMediaPlayer::SetVideoSourceRect
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
 - IMFPMediaPlayer.SetVideoSourceRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfplay.h
: 
- IMFPMediaPlayer.SetVideoSourceRect
: 
---

# IMFPMediaPlayer::SetVideoSourceRect


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Sets the video source rectangle.

MFPlay clips the video to this rectangle and stretches the rectangle to fill the video window.


## -parameters




### -param pnrcSource [in]

Pointer to an <a href="https://msdn.microsoft.com/c1dd42ca-64a0-4f30-82e1-eda3f4721526">MFVideoNormalizedRect</a> structure that specifies the source rectangle. This rectangle defines which portion of the video is displayed. It is specified in normalized coordinates, which are defined as follows:

<ul>
<li>The upper-left corner of the video image is (0, 0).</li>
<li>The lower-right corner of  the video image is (1, 1).</li>
</ul>
To display the entire image, set the source rectangle to {0, 0, 1, 1}. This is the default value.


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
The object's <a href="https://msdn.microsoft.com/c56b07b5-f595-4933-9af6-868fc8938849">Shutdown</a> method was called.

</td>
</tr>
</table>
 




## -remarks



MFPlay stretches the source rectangle to fill the entire video window. By default, MFPlay maintains the source's correct aspect ratio, letterboxing if needed. The letterbox color is controlled by the <a href="https://msdn.microsoft.com/f66b671d-0c7d-4261-8210-05f2d2f8d9a5">IMFPMediaPlayer::SetBorderColor</a> method.

This method fails if no media item is currently set, or if the current media item does not contain video.

To set the video position before playback starts, call this method inside your event handler for the <b>MFP_EVENT_TYPE_MEDIAITEM_SET</b> event. For more information, see <a href="https://msdn.microsoft.com/2a80a9d0-83ee-4bb0-ab2c-0f68367f3bf8">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

