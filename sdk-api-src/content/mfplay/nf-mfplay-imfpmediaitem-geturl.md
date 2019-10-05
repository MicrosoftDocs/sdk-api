---
UID: NF:mfplay.IMFPMediaItem.GetURL
title: IMFPMediaItem::GetURL (mfplay.h)
author: windows-sdk-content
description: Gets the URL that was used to create the media item.
old-location: mf\imfpmediaitem_geturl.htm
tech.root: medfound
ms.assetid: 2598534c-28cc-4f4c-bf87-17ab7044e0c1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetURL, GetURL method [Media Foundation], GetURL method [Media Foundation],IMFPMediaItem interface, IMFPMediaItem interface [Media Foundation],GetURL method, IMFPMediaItem.GetURL, IMFPMediaItem::GetURL, mf.imfpmediaitem_geturl, mfplay/IMFPMediaItem::GetURL
ms.topic: method
f1_keywords: 
 - "mfplay/IMFPMediaItem.GetURL"
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
 - IMFPMediaItem.GetURL
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPMediaItem::GetURL


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Gets the URL that was used to create the media item.


## -parameters




### -param ppwszURL [out]

Receives a pointer to a null-terminated string that contains the URL. The caller must free the string by calling <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.


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
<dt><b>MF_E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
No URL is associated with this media item.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown">IMFPMediaPlayer::Shutdown</a> method was called.

</td>
</tr>
</table>
 




## -remarks



This method applies when the application calls  <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl">IMFPMediaPlayer::CreateMediaItemFromURL</a> to create a media item. If the application calls <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject">IMFPMediaPlayer::CreateMediaItemFromObject</a> to create a media item, the  <b>GetURL</b> method for that media item returns  <b>MF_E_NOTFOUND</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl">IMFPMediaPlayer::CreateMediaItemFromURL</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
 

 

