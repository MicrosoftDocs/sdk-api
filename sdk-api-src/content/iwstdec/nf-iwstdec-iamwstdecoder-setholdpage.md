---
UID: NF:iwstdec.IAMWstDecoder.SetHoldPage
title: IAMWstDecoder::SetHoldPage (iwstdec.h)
description: Downstream filters use the SetHoldPage method to tell the WST decoder to hold the current WST page. When the WST decoder holds a page, any updates from the TV stream are turned off. It is as though the page was paused in real time.
helpviewer_keywords: ["IAMWstDecoder interface [DirectShow]","SetHoldPage method","IAMWstDecoder.SetHoldPage","IAMWstDecoder::SetHoldPage","IAMWstDecoderSetHoldPage","SetHoldPage","SetHoldPage method [DirectShow]","SetHoldPage method [DirectShow]","IAMWstDecoder interface","dshow.iamwstdecoder_setholdpage","iwstdec/IAMWstDecoder::SetHoldPage"]
old-location: dshow\iamwstdecoder_setholdpage.htm
tech.root: dshow
ms.assetid: 2fea6f52-bae3-4679-a89b-fe85f1232d34
ms.date: 4/26/2023
ms.keywords: IAMWstDecoder interface [DirectShow],SetHoldPage method, IAMWstDecoder.SetHoldPage, IAMWstDecoder::SetHoldPage, IAMWstDecoderSetHoldPage, SetHoldPage, SetHoldPage method [DirectShow], SetHoldPage method [DirectShow],IAMWstDecoder interface, dshow.iamwstdecoder_setholdpage, iwstdec/IAMWstDecoder::SetHoldPage
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
 - IAMWstDecoder::SetHoldPage
 - iwstdec/IAMWstDecoder::SetHoldPage
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
 - IAMWstDecoder.SetHoldPage
---

# IAMWstDecoder::SetHoldPage


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Downstream filters use the <code>SetHoldPage</code> method to tell the WST decoder to hold the current WST page. When the WST decoder holds a page, any updates from the TV stream are turned off. It is as though the page was paused in real time.

## -parameters

### -param bHoldPage [in]

Specifies whether to hold the current page.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>Hold the current page</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>Release the current page.</td>
</tr>
</table>

## -returns

When the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/iwstdec/nn-iwstdec-iamwstdecoder">IAMWstDecoder Interface</a>