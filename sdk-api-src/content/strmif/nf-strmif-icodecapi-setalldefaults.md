---
UID: NF:strmif.ICodecAPI.SetAllDefaults
title: ICodecAPI::SetAllDefaults (strmif.h)
description: The SetAllDefaults method resets all codec properties to their default values. (ICodecAPI.SetAllDefaults)
helpviewer_keywords: ["ICodecAPI interface [DirectShow]","SetAllDefaults method","ICodecAPI.SetAllDefaults","ICodecAPI::SetAllDefaults","ICodecAPISetAllDefaults","SetAllDefaults","SetAllDefaults method [DirectShow]","SetAllDefaults method [DirectShow]","ICodecAPI interface","dshow.icodecapi_setalldefaults","strmif/ICodecAPI::SetAllDefaults"]
old-location: dshow\icodecapi_setalldefaults.htm
tech.root: dshow
ms.assetid: b2f630be-a105-4f1b-9f9a-9d56c8853f35
ms.date: 4/26/2023
ms.keywords: ICodecAPI interface [DirectShow],SetAllDefaults method, ICodecAPI.SetAllDefaults, ICodecAPI::SetAllDefaults, ICodecAPISetAllDefaults, SetAllDefaults, SetAllDefaults method [DirectShow], SetAllDefaults method [DirectShow],ICodecAPI interface, dshow.icodecapi_setalldefaults, strmif/ICodecAPI::SetAllDefaults
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
 - ICodecAPI::SetAllDefaults
 - strmif/ICodecAPI::SetAllDefaults
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
 - ICodecAPI.SetAllDefaults
---

# ICodecAPI::SetAllDefaults


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetAllDefaults</b> method resets all codec properties to their default values.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-reference">Codec API Reference</a>



<a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a>



<a href="/windows/desktop/api/strmif/nf-strmif-icodecapi-getvalue">ICodecAPI::GetValue</a>
