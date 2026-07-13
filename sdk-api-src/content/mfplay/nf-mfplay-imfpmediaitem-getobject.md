---
UID: NF:mfplay.IMFPMediaItem.GetObject
title: IMFPMediaItem::GetObject (mfplay.h)
description: Gets the object that was used to create the media item.
helpviewer_keywords: ["GetObject","GetObject method [Media Foundation]","GetObject method [Media Foundation]","IMFPMediaItem interface","IMFPMediaItem interface [Media Foundation]","GetObject method","IMFPMediaItem.GetObject","IMFPMediaItem::GetObject","mf.imfpmediaitem_getobject","mfplay/IMFPMediaItem::GetObject"]
old-location: mf\imfpmediaitem_getobject.htm
tech.root: mfarchive
archived: true
ms.assetid: 6a6abc57-149d-4e4b-a29f-7b712d24e6df
ms.date: 12/05/2018
ms.keywords: GetObject, GetObject method [Media Foundation], GetObject method [Media Foundation],IMFPMediaItem interface, IMFPMediaItem interface [Media Foundation],GetObject method, IMFPMediaItem.GetObject, IMFPMediaItem::GetObject, mf.imfpmediaitem_getobject, mfplay/IMFPMediaItem::GetObject
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
 - IMFPMediaItem::GetObject
 - mfplay/IMFPMediaItem::GetObject
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
 - IMFPMediaItem.GetObject
---

# IMFPMediaItem::GetObject


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Gets the object that was used to create the media item.

## -parameters

### -param ppIUnknown [out]

Receives a pointer to the object's <b>IUnknown</b> interface. The caller must release the interface.

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
The media item was created from a URL, not from an object.

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

The object pointer is set if the application uses <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject">IMFPMediaPlayer::CreateMediaItemFromObject</a> to create the media item. Otherwise, <b>GetObject</b> returns  MF_E_NOTFOUND.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>