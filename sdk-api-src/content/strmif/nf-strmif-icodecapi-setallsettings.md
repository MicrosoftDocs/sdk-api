---
UID: NF:strmif.ICodecAPI.SetAllSettings
title: ICodecAPI::SetAllSettings (strmif.h)
description: The SetAllSettings method reads codec properties from a stream and sets them on the codec. (ICodecAPI.SetAllSettings)
helpviewer_keywords: ["ICodecAPI interface [DirectShow]","SetAllSettings method","ICodecAPI.SetAllSettings","ICodecAPI::SetAllSettings","ICodecAPISetAllSettings","SetAllSettings","SetAllSettings method [DirectShow]","SetAllSettings method [DirectShow]","ICodecAPI interface","dshow.icodecapi_setallsettings","strmif/ICodecAPI::SetAllSettings"]
old-location: dshow\icodecapi_setallsettings.htm
tech.root: dshow
ms.assetid: 1148e380-a4fc-4392-861e-8ea695060032
ms.date: 4/26/2023
ms.keywords: ICodecAPI interface [DirectShow],SetAllSettings method, ICodecAPI.SetAllSettings, ICodecAPI::SetAllSettings, ICodecAPISetAllSettings, SetAllSettings, SetAllSettings method [DirectShow], SetAllSettings method [DirectShow],ICodecAPI interface, dshow.icodecapi_setallsettings, strmif/ICodecAPI::SetAllSettings
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICodecAPI::SetAllSettings
 - strmif/ICodecAPI::SetAllSettings
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - ICodecAPI.SetAllSettings
---

# ICodecAPI::SetAllSettings


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetAllSettings</b> method reads codec properties from a stream and sets them on the codec.

## -parameters

### -param __MIDL__ICodecAPI0001 [in]

Pointer to the <b>IStream</b> interface of the stream.

## -returns

This method can return one of these values.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
</table>

## -remarks

Codecs that implement <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a> are  not required to support this method.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-reference">Codec API Reference</a>



<a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a>



<a href="/windows/desktop/api/strmif/nf-strmif-icodecapi-getvalue">ICodecAPI::GetValue</a>
