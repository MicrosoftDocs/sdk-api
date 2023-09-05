---
UID: NF:iwstdec.IAMWstDecoder.GetDecoderLevel
title: IAMWstDecoder::GetDecoderLevel (iwstdec.h)
description: Applications use the GetDecoderLevel method to retrieve the WST decoder level. This method is not implemented and always returns AM_WST_LEVEL_1_5.
helpviewer_keywords: ["GetDecoderLevel","GetDecoderLevel method [DirectShow]","GetDecoderLevel method [DirectShow]","IAMWstDecoder interface","IAMWstDecoder interface [DirectShow]","GetDecoderLevel method","IAMWstDecoder.GetDecoderLevel","IAMWstDecoder::GetDecoderLevel","IAMWstDecoderGetDecoderLevel","dshow.iamwstdecoder_getdecoderlevel","iwstdec/IAMWstDecoder::GetDecoderLevel"]
old-location: dshow\iamwstdecoder_getdecoderlevel.htm
tech.root: dshow
ms.assetid: 629ee71d-7d79-4fa9-b169-3b5328659435
ms.date: 4/26/2023
ms.keywords: GetDecoderLevel, GetDecoderLevel method [DirectShow], GetDecoderLevel method [DirectShow],IAMWstDecoder interface, IAMWstDecoder interface [DirectShow],GetDecoderLevel method, IAMWstDecoder.GetDecoderLevel, IAMWstDecoder::GetDecoderLevel, IAMWstDecoderGetDecoderLevel, dshow.iamwstdecoder_getdecoderlevel, iwstdec/IAMWstDecoder::GetDecoderLevel
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
 - IAMWstDecoder::GetDecoderLevel
 - iwstdec/IAMWstDecoder::GetDecoderLevel
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
 - IAMWstDecoder.GetDecoderLevel
---

# IAMWstDecoder::GetDecoderLevel


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Applications use the <code>GetDecoderLevel</code> method to retrieve the WST decoder level. This method is not implemented and always returns AM_WST_LEVEL_1_5.

## -parameters

### -param lpLevel [out]

Receives a member of the <a href="/previous-versions/windows/desktop/api/iwstdec/ne-iwstdec-am_wst_level">AM_WST_LEVEL</a> enumeration, indicating the decoder level.

## -returns

When the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/iwstdec/nn-iwstdec-iamwstdecoder">IAMWstDecoder Interface</a>