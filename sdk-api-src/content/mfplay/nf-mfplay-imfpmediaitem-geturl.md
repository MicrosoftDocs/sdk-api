---
UID: NF:mfplay.IMFPMediaItem.GetURL
title: IMFPMediaItem::GetURL (mfplay.h)
description: Gets the URL that was used to create the media item.
helpviewer_keywords: ["GetURL","GetURL method [Media Foundation]","GetURL method [Media Foundation]","IMFPMediaItem interface","IMFPMediaItem interface [Media Foundation]","GetURL method","IMFPMediaItem.GetURL","IMFPMediaItem::GetURL","mf.imfpmediaitem_geturl","mfplay/IMFPMediaItem::GetURL"]
old-location: mf\imfpmediaitem_geturl.htm
tech.root: mfarchive
archived: true
ms.assetid: 2598534c-28cc-4f4c-bf87-17ab7044e0c1
ms.date: 12/05/2018
ms.keywords: GetURL, GetURL method [Media Foundation], GetURL method [Media Foundation],IMFPMediaItem interface, IMFPMediaItem interface [Media Foundation],GetURL method, IMFPMediaItem.GetURL, IMFPMediaItem::GetURL, mf.imfpmediaitem_geturl, mfplay/IMFPMediaItem::GetURL
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFPMediaItem::GetURL
 - mfplay/IMFPMediaItem::GetURL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplay.h
api_name:
 - IMFPMediaItem.GetURL
---

# IMFPMediaItem::GetURL


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Gets the URL that was used to create the media item.

## -parameters

### -param ppwszURL [out]

Receives a pointer to a null-terminated string that contains the URL. The caller must free the string by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

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
The <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown">IMFPMediaPlayer::Shutdown</a> method was called.

</td>
</tr>
</table>

## -remarks

This method applies when the application calls  <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl">IMFPMediaPlayer::CreateMediaItemFromURL</a> to create a media item. If the application calls <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject">IMFPMediaPlayer::CreateMediaItemFromObject</a> to create a media item, the  <b>GetURL</b> method for that media item returns  <b>MF_E_NOTFOUND</b>.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a>



<a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl">IMFPMediaPlayer::CreateMediaItemFromURL</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>