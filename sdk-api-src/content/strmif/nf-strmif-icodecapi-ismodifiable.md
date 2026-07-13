---
UID: NF:strmif.ICodecAPI.IsModifiable
title: ICodecAPI::IsModifiable (strmif.h)
description: The IsModifiable method queries whether a codec property can be changed, given the codec's current configuration. (ICodecAPI.IsModifiable)
helpviewer_keywords: ["ICodecAPI interface [DirectShow]","IsModifiable method","ICodecAPI.IsModifiable","ICodecAPI::IsModifiable","ICodecAPIIsModifiable","IsModifiable","IsModifiable method [DirectShow]","IsModifiable method [DirectShow]","ICodecAPI interface","dshow.icodecapi_ismodifiable","strmif/ICodecAPI::IsModifiable"]
old-location: dshow\icodecapi_ismodifiable.htm
tech.root: dshow
ms.assetid: 5f7c7f72-02f2-4840-aaa2-9d26fe564577
ms.date: 4/26/2023
ms.keywords: ICodecAPI interface [DirectShow],IsModifiable method, ICodecAPI.IsModifiable, ICodecAPI::IsModifiable, ICodecAPIIsModifiable, IsModifiable, IsModifiable method [DirectShow], IsModifiable method [DirectShow],ICodecAPI interface, dshow.icodecapi_ismodifiable, strmif/ICodecAPI::IsModifiable
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
 - ICodecAPI::IsModifiable
 - strmif/ICodecAPI::IsModifiable
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
 - ICodecAPI.IsModifiable
---

# ICodecAPI::IsModifiable


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IsModifiable</b> method queries whether a codec property can be changed, given the codec's current configuration.

## -parameters

### -param Api [in]

Pointer to a GUID that specifies the property. For a list of standard codec properties, see <a href="/windows/desktop/DirectShow/codec-api-properties">Codec API Properties</a>.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The value of this property cannot be changed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The value of this property can be changed.

</td>
</tr>
</table>

## -remarks

Any errors besides those in the previous table indicate an inability to process the call.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-reference">Codec API Reference</a>



<a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a>
