---
UID: NF:il21dec.IAMLine21Decoder.SetRedrawAlways
title: IAMLine21Decoder::SetRedrawAlways (il21dec.h)
description: The SetRedrawAlways method specifies whether the Line 21 Decoder filter redraws the entire output bitmap for each sample.
helpviewer_keywords: ["IAMLine21Decoder interface [DirectShow]","SetRedrawAlways method","IAMLine21Decoder.SetRedrawAlways","IAMLine21Decoder::SetRedrawAlways","IAMLine21DecoderSetRedrawAlways","SetRedrawAlways","SetRedrawAlways method [DirectShow]","SetRedrawAlways method [DirectShow]","IAMLine21Decoder interface","dshow.iamline21decoder_setredrawalways","il21dec/IAMLine21Decoder::SetRedrawAlways"]
old-location: dshow\iamline21decoder_setredrawalways.htm
tech.root: dshow
ms.assetid: 20f2e95a-8362-457d-b562-f7263e698551
ms.date: 4/26/2023
ms.keywords: IAMLine21Decoder interface [DirectShow],SetRedrawAlways method, IAMLine21Decoder.SetRedrawAlways, IAMLine21Decoder::SetRedrawAlways, IAMLine21DecoderSetRedrawAlways, SetRedrawAlways, SetRedrawAlways method [DirectShow], SetRedrawAlways method [DirectShow],IAMLine21Decoder interface, dshow.iamline21decoder_setredrawalways, il21dec/IAMLine21Decoder::SetRedrawAlways
req.header: il21dec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IAMLine21Decoder::SetRedrawAlways
 - il21dec/IAMLine21Decoder::SetRedrawAlways
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
 - IAMLine21Decoder.SetRedrawAlways
---

# IAMLine21Decoder::SetRedrawAlways


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetRedrawAlways</code> method specifies whether the <a href="/windows/desktop/DirectShow/line-21-decoder-filter">Line 21 Decoder</a> filter redraws the entire output bitmap for each sample.

## -parameters

### -param bOption

Specifies one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>The filter always redraws the entire bitmap.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>The filter does not always redraw the entire bitmap. (Default)</td>
</tr>
</table>

## -returns

Returns S_OK if successful, or an error code otherwise.

## -remarks

Generally, applications should not call this method. The downstream mixer or renderer filter should call this method with the value <b>TRUE</b> if it writes into the buffers that it receives from the <a href="/windows/desktop/DirectShow/line-21-decoder-filter">Line 21 Decoder</a> filter. Redrawing degrades performance and increases CPU load, because it negates any potential optimizations.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder">IAMLine21Decoder Interface</a>



<a href="/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-getredrawalways">IAMLine21Decoder::GetRedrawAlways</a>