---
UID: NF:iwstdec.IAMWstDecoder.GetHoldPage
title: IAMWstDecoder::GetHoldPage (iwstdec.h)
description: Downstream filters use the GetHoldPage method to determine whether the current WST page is held. When the WST decoder holds a page, any updates from the TV stream are turned off. It is though the page was paused in real time.
helpviewer_keywords: ["GetHoldPage","GetHoldPage method [DirectShow]","GetHoldPage method [DirectShow]","IAMWstDecoder interface","IAMWstDecoder interface [DirectShow]","GetHoldPage method","IAMWstDecoder.GetHoldPage","IAMWstDecoder::GetHoldPage","IAMWstDecoderGetHoldPage","dshow.iamwstdecoder_getholdpage","iwstdec/IAMWstDecoder::GetHoldPage"]
old-location: dshow\iamwstdecoder_getholdpage.htm
tech.root: dshow
ms.assetid: db09b2a2-7f92-421a-8582-4ed648563119
ms.date: 4/26/2023
ms.keywords: GetHoldPage, GetHoldPage method [DirectShow], GetHoldPage method [DirectShow],IAMWstDecoder interface, IAMWstDecoder interface [DirectShow],GetHoldPage method, IAMWstDecoder.GetHoldPage, IAMWstDecoder::GetHoldPage, IAMWstDecoderGetHoldPage, dshow.iamwstdecoder_getholdpage, iwstdec/IAMWstDecoder::GetHoldPage
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
 - IAMWstDecoder::GetHoldPage
 - iwstdec/IAMWstDecoder::GetHoldPage
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
 - IAMWstDecoder.GetHoldPage
---

# IAMWstDecoder::GetHoldPage


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Downstream filters use the <code>GetHoldPage</code> method to determine whether the current WST page is held. When the WST decoder holds a page, any updates from the TV stream are turned off. It is though the page was paused in real time.

## -parameters

### -param pbHoldPage [out]

Pointer to a <b>BOOL</b> to receive the status of the WST page.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>The current page is held.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>The current page is not held.</td>
</tr>
</table>

## -returns

When the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/iwstdec/nn-iwstdec-iamwstdecoder">IAMWstDecoder Interface</a>