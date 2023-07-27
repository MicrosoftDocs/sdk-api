---
UID: NF:iwstdec.IAMWstDecoder.SetBackgroundColor
title: IAMWstDecoder::SetBackgroundColor (iwstdec.h)
description: Downstream filters use the SetBackgroundColor method to assign the physical color to be used in color keying the background for overlay mixing.
helpviewer_keywords: ["IAMWstDecoder interface [DirectShow]","SetBackgroundColor method","IAMWstDecoder.SetBackgroundColor","IAMWstDecoder::SetBackgroundColor","IAMWstDecoderSetBackgroundColor","SetBackgroundColor","SetBackgroundColor method [DirectShow]","SetBackgroundColor method [DirectShow]","IAMWstDecoder interface","dshow.iamwstdecoder_setbackgroundcolor","iwstdec/IAMWstDecoder::SetBackgroundColor"]
old-location: dshow\iamwstdecoder_setbackgroundcolor.htm
tech.root: dshow
ms.assetid: d65726aa-a826-41d4-95f3-40c86d7b9347
ms.date: 4/26/2023
ms.keywords: IAMWstDecoder interface [DirectShow],SetBackgroundColor method, IAMWstDecoder.SetBackgroundColor, IAMWstDecoder::SetBackgroundColor, IAMWstDecoderSetBackgroundColor, SetBackgroundColor, SetBackgroundColor method [DirectShow], SetBackgroundColor method [DirectShow],IAMWstDecoder interface, dshow.iamwstdecoder_setbackgroundcolor, iwstdec/IAMWstDecoder::SetBackgroundColor
req.header: iwstdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IAMWstDecoder::SetBackgroundColor
 - iwstdec/IAMWstDecoder::SetBackgroundColor
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
 - IAMWstDecoder.SetBackgroundColor
---

# IAMWstDecoder::SetBackgroundColor


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Downstream filters use the <code>SetBackgroundColor</code> method to assign the physical color to be used in color keying the background for overlay mixing.

## -parameters

### -param dwPhysColor [in]

Specifies a <b>DWORD</b> containing the physical color.

## -returns

When the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/iwstdec/nn-iwstdec-iamwstdecoder">IAMWstDecoder Interface</a>