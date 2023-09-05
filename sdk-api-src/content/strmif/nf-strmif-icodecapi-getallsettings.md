---
UID: NF:strmif.ICodecAPI.GetAllSettings
title: ICodecAPI::GetAllSettings (strmif.h)
description: The GetAllSettings method gets the codec's current properties and writes them to a stream. (ICodecAPI.GetAllSettings)
helpviewer_keywords: ["GetAllSettings","GetAllSettings method [DirectShow]","GetAllSettings method [DirectShow]","ICodecAPI interface","ICodecAPI interface [DirectShow]","GetAllSettings method","ICodecAPI.GetAllSettings","ICodecAPI::GetAllSettings","ICodecAPIGetAllSettings","dshow.icodecapi_getallsettings","strmif/ICodecAPI::GetAllSettings"]
old-location: dshow\icodecapi_getallsettings.htm
tech.root: dshow
ms.assetid: 45685033-73cc-4810-90f2-49343494641b
ms.date: 4/26/2023
ms.keywords: GetAllSettings, GetAllSettings method [DirectShow], GetAllSettings method [DirectShow],ICodecAPI interface, ICodecAPI interface [DirectShow],GetAllSettings method, ICodecAPI.GetAllSettings, ICodecAPI::GetAllSettings, ICodecAPIGetAllSettings, dshow.icodecapi_getallsettings, strmif/ICodecAPI::GetAllSettings
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
 - ICodecAPI::GetAllSettings
 - strmif/ICodecAPI::GetAllSettings
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
 - ICodecAPI.GetAllSettings
---

# ICodecAPI::GetAllSettings


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetAllSettings</b> method gets the codec's current properties and writes them to  a stream.

## -parameters

### -param __MIDL__ICodecAPI0000 [in]

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

To load the properties from the stream back onto the codec, call <a href="/windows/desktop/api/strmif/nf-strmif-icodecapi-setallsettings">ICodecAPI::SetAllSettings</a> or <a href="/windows/desktop/api/strmif/nf-strmif-icodecapi-setallsettingswithnotify">ICodecAPI::SetAllSettingsWithNotify</a>.

The format of the data that is written to the stream depends on the implementation of the codec. There is no standard serialization format.  An application should not attempt to save the properties from one codec and load them on a different codec.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-reference">Codec API Reference</a>



<a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a>
