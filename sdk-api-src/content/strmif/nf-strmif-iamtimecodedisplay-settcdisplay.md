---
UID: NF:strmif.IAMTimecodeDisplay.SetTCDisplay
title: IAMTimecodeDisplay::SetTCDisplay (strmif.h)
description: The SetTCDisplay method sets the timecode character generator output characteristics.
helpviewer_keywords: ["IAMTimecodeDisplay interface [DirectShow]","SetTCDisplay method","IAMTimecodeDisplay.SetTCDisplay","IAMTimecodeDisplay::SetTCDisplay","IAMTimecodeDisplaySetTCDisplay","SetTCDisplay","SetTCDisplay method [DirectShow]","SetTCDisplay method [DirectShow]","IAMTimecodeDisplay interface","dshow.iamtimecodedisplay_settcdisplay","strmif/IAMTimecodeDisplay::SetTCDisplay"]
old-location: dshow\iamtimecodedisplay_settcdisplay.htm
tech.root: dshow
ms.assetid: 34d55c5a-d213-4fb2-b81c-b117d025f3ec
ms.date: 4/26/2023
ms.keywords: IAMTimecodeDisplay interface [DirectShow],SetTCDisplay method, IAMTimecodeDisplay.SetTCDisplay, IAMTimecodeDisplay::SetTCDisplay, IAMTimecodeDisplaySetTCDisplay, SetTCDisplay, SetTCDisplay method [DirectShow], SetTCDisplay method [DirectShow],IAMTimecodeDisplay interface, dshow.iamtimecodedisplay_settcdisplay, strmif/IAMTimecodeDisplay::SetTCDisplay
req.header: strmif.h
req.include-header: Dshow.h
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
 - IAMTimecodeDisplay::SetTCDisplay
 - strmif/IAMTimecodeDisplay::SetTCDisplay
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
 - IAMTimecodeDisplay.SetTCDisplay
---

# IAMTimecodeDisplay::SetTCDisplay


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetTCDisplay</code> method sets the timecode character generator output characteristics.

## -parameters

### -param Param [in]

Timecode display characteristic. Specify one of the following properties you want to set properties for.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_TCD_BORDER</td>
<td>White border for black characters, black border for white characters</td>
</tr>
<tr>
<td>ED_TCD_INTENSITY</td>
<td>Intensity (brightness) of characters</td>
</tr>
<tr>
<td>ED_TCD_INVERT</td>
<td>Black characters on white background or white characters on black background</td>
</tr>
<tr>
<td>ED_TCD_POSITION</td>
<td>Position of characters</td>
</tr>
<tr>
<td>ED_TCD_SIZE</td>
<td>Size of characters</td>
</tr>
<tr>
<td>ED_TCD_SOURCE</td>
<td>Source of the display's data</td>
</tr>
<tr>
<td>ED_TCD_TRANSPARENCY</td>
<td>Transparency of characters</td>
</tr>
</table>

### -param Value [in]

Setting of the parameter specified in <i>Param</i>. Must be one of the following:

If ED_TCD_SOURCE specified in <i>Param</i>, set one of the following.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_TCG</td>
<td>Timecode generator</td>
</tr>
<tr>
<td>ED_TCR</td>
<td>Timecode reader</td>
</tr>
</table>
 

If ED_TCD_SIZE is specified in <i>Param</i>, set one of the following.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_LARGE</td>
<td>Large</td>
</tr>
<tr>
<td>ED_MED</td>
<td>Medium</td>
</tr>
<tr>
<td>ED_SMALL</td>
<td>Small</td>
</tr>
</table>
 

If ED_TCD_POSITION specified in <i>Param</i>, set one of the following.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_BOTTOM</td>
<td>Bottom</td>
</tr>
<tr>
<td>ED_MIDDLE</td>
<td>Middle</td>
</tr>
<tr>
<td>ED_TOP</td>
<td>Top</td>
</tr>
</table>
 

in combination with one of the following.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_CENTER</td>
<td>Center</td>
</tr>
<tr>
<td>ED_LEFT</td>
<td>Left</td>
</tr>
<tr>
<td>ED_RIGHT</td>
<td>Right</td>
</tr>
</table>
 

If ED_TCD_INTENSITY is specified in <i>Param</i>, set one of the following.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_HIGH</td>
<td>High</td>
</tr>
<tr>
<td>ED_LOW</td>
<td>Low</td>
</tr>
</table>
 

If ED_TCD_TRANSPARENCY is specified in <i>Param</i>, set a value from 0 to 4, 0 being completely opaque, 4 being as dark as possible.

If ED_TCD_INVERT is specified in <i>Param</i>, set one of the following.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>OAFALSE</td>
<td>Black on white</td>
</tr>
<tr>
<td>OATRUE</td>
<td>White on black</td>
</tr>
</table>
 

If ED_TCD_BORDER is specified in <i>Param</i>, set one of the following.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>OAFALSE</td>
<td>Black characters for white border</td>
</tr>
<tr>
<td>OATRUE</td>
<td>White border for black characters</td>
</tr>
</table>

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtimecodedisplay">IAMTimecodeDisplay Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamtimecodedisplay-gettcdisplay">IAMTimecodeDisplay::GetTCDisplay</a>