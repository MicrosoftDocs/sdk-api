---
UID: NF:mfplay.IMFPMediaPlayer.GetMediaItem
title: IMFPMediaPlayer::GetMediaItem
author: windows-sdk-content
description: Gets a pointer to the current media item.
old-location: mf\imfpmediaplayer_getmediaitem.htm
tech.root: medfound
ms.assetid: 9593092d-bd50-4ff6-a283-f5a0ab1e6fc0
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetMediaItem, GetMediaItem method [Media Foundation], GetMediaItem method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],GetMediaItem method, IMFPMediaPlayer.GetMediaItem, IMFPMediaPlayer::GetMediaItem, mf.imfpmediaplayer_getmediaitem, mfplay/IMFPMediaPlayer::GetMediaItem
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
 - IMFPMediaPlayer.GetMediaItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMediaPlayer::GetMediaItem


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Gets a pointer to the current media item.


## -parameters




### -param ppIMFPMediaItem [out]

Receives a pointer to the media item's <a href="https://msdn.microsoft.com/2839d256-bdaf-40cf-9f9d-46f9e2ce59e8">IMFPMediaItem</a> interface. The caller must release the interface.


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
<dt><b><b>E_FAIL</b></b></dt>
</dl>
</td>
<td width="60%">
There is no current media item.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_NOT_FOUND</b></b></dt>
</dl>
</td>
<td width="60%">
There is no current media item.

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



The <a href="https://msdn.microsoft.com/c792a024-c4f8-4e0b-9720-259d1dc28ee8">IMFPMediaPlayer::SetMediaItem</a> method is asynchronous. Therefore, while <b>SetMediaItem</b> is pending, <b>GetMediaItem</b> will not return the media item that was just set. Instead, the application should implement <a href="https://msdn.microsoft.com/7d9d01bf-861a-4c35-93b1-dbf85cbf0a32">IMFPMediaPlayerCallback</a> interface and handle the <b>MFP_EVENT_TYPE_MEDIAITEM_SET</b> event. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Dd318791(v=VS.85).aspx">Receiving Events From the Player</a>.

The previous remark also applies to setting the media item in the <a href="https://msdn.microsoft.com/80c668e2-5e93-4af2-871c-646228e18717">MFPCreateMediaPlayer</a> function.




## -see-also




<a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

