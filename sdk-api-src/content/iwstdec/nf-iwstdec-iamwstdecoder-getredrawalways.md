---
UID: NF:iwstdec.IAMWstDecoder.GetRedrawAlways
title: IAMWstDecoder::GetRedrawAlways (iwstdec.h)
description: Downstream filters use the GetRedrawAlways method to retrieve a value that indicates whether the whole output bitmap is redrawn for each sample.
helpviewer_keywords: ["GetRedrawAlways","GetRedrawAlways method [DirectShow]","GetRedrawAlways method [DirectShow]","IAMWstDecoder interface","IAMWstDecoder interface [DirectShow]","GetRedrawAlways method","IAMWstDecoder.GetRedrawAlways","IAMWstDecoder::GetRedrawAlways","IAMWstDecoderGetRedrawAlways","dshow.iamwstdecoder_getredrawalways","iwstdec/IAMWstDecoder::GetRedrawAlways"]
old-location: dshow\iamwstdecoder_getredrawalways.htm
tech.root: dshow
ms.assetid: d4035bd0-9a86-4deb-b4eb-4aa5b4b4ff35
ms.date: 4/26/2023
ms.keywords: GetRedrawAlways, GetRedrawAlways method [DirectShow], GetRedrawAlways method [DirectShow],IAMWstDecoder interface, IAMWstDecoder interface [DirectShow],GetRedrawAlways method, IAMWstDecoder.GetRedrawAlways, IAMWstDecoder::GetRedrawAlways, IAMWstDecoderGetRedrawAlways, dshow.iamwstdecoder_getredrawalways, iwstdec/IAMWstDecoder::GetRedrawAlways
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
 - IAMWstDecoder::GetRedrawAlways
 - iwstdec/IAMWstDecoder::GetRedrawAlways
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
 - IAMWstDecoder.GetRedrawAlways
---

# IAMWstDecoder::GetRedrawAlways


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Downstream filters use the <code>GetRedrawAlways</code> method to retrieve a value that indicates whether the whole output bitmap is redrawn for each sample.

## -parameters

### -param lpbOption [out]

Pointer to a <b>BOOL</b> to receive the redraw-always value.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>Redraw the whole output bitmap for each sample.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>Do not redraw the whole output bitmap for each sample.</td>
</tr>
</table>

## -returns

When the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/iwstdec/nn-iwstdec-iamwstdecoder">IAMWstDecoder Interface</a>