---
UID: NF:iwstdec.IAMWstDecoder.GetCurrentPage
title: IAMWstDecoder::GetCurrentPage (iwstdec.h)
description: Downstream filters use the GetCurrentPage method to retrieve the current WST page.
helpviewer_keywords: ["GetCurrentPage","GetCurrentPage method [DirectShow]","GetCurrentPage method [DirectShow]","IAMWstDecoder interface","IAMWstDecoder interface [DirectShow]","GetCurrentPage method","IAMWstDecoder.GetCurrentPage","IAMWstDecoder::GetCurrentPage","IAMWstDecoderGetCurrentPage","dshow.iamwstdecoder_getcurrentpage","iwstdec/IAMWstDecoder::GetCurrentPage"]
old-location: dshow\iamwstdecoder_getcurrentpage.htm
tech.root: dshow
ms.assetid: e4e52723-27ad-487a-a547-7ad7ade6f099
ms.date: 4/26/2023
ms.keywords: GetCurrentPage, GetCurrentPage method [DirectShow], GetCurrentPage method [DirectShow],IAMWstDecoder interface, IAMWstDecoder interface [DirectShow],GetCurrentPage method, IAMWstDecoder.GetCurrentPage, IAMWstDecoder::GetCurrentPage, IAMWstDecoderGetCurrentPage, dshow.iamwstdecoder_getcurrentpage, iwstdec/IAMWstDecoder::GetCurrentPage
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
 - IAMWstDecoder::GetCurrentPage
 - iwstdec/IAMWstDecoder::GetCurrentPage
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
 - IAMWstDecoder.GetCurrentPage
---

# IAMWstDecoder::GetCurrentPage


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Downstream filters use the <code>GetCurrentPage</code> method to retrieve the current WST page.

## -parameters

### -param pWstPage [out]

A pointer to an <a href="/previous-versions/windows/desktop/api/iwstdec/ns-iwstdec-am_wst_page">AM_WST_PAGE</a> structure to receive the current page.

## -returns

When the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/iwstdec/nn-iwstdec-iamwstdecoder">IAMWstDecoder Interface</a>