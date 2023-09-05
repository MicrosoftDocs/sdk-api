---
UID: NF:strmif.IAMCrossbar.get_PinCounts
title: IAMCrossbar::get_PinCounts (strmif.h)
description: The get_PinCounts method retrieves the number of input and output pins on the crossbar filter.
helpviewer_keywords: ["IAMCrossbar interface [DirectShow]","get_PinCounts method","IAMCrossbar.get_PinCounts","IAMCrossbar::get_PinCounts","IAMCrossbarget_PinCounts","dshow.iamcrossbar_get_pincounts","get_PinCounts","get_PinCounts method [DirectShow]","get_PinCounts method [DirectShow]","IAMCrossbar interface","strmif/IAMCrossbar::get_PinCounts"]
old-location: dshow\iamcrossbar_get_pincounts.htm
tech.root: dshow
ms.assetid: 66ea86a6-82c3-4f91-a2d3-a08014f555be
ms.date: 4/26/2023
ms.keywords: IAMCrossbar interface [DirectShow],get_PinCounts method, IAMCrossbar.get_PinCounts, IAMCrossbar::get_PinCounts, IAMCrossbarget_PinCounts, dshow.iamcrossbar_get_pincounts, get_PinCounts, get_PinCounts method [DirectShow], get_PinCounts method [DirectShow],IAMCrossbar interface, strmif/IAMCrossbar::get_PinCounts
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
 - IAMCrossbar::get_PinCounts
 - strmif/IAMCrossbar::get_PinCounts
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
 - IAMCrossbar.get_PinCounts
---

# IAMCrossbar::get_PinCounts


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_PinCounts</code> method retrieves the number of input and output pins on the crossbar filter.

## -parameters

### -param OutputPinCount [out]

Pointer to variable that receives the number of output pins.

### -param InputPinCount [out]

Pointer to variable that receives the number of input pins.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>

## -remarks

The other <a href="/windows/desktop/api/strmif/nn-strmif-iamcrossbar">IAMCrossbar</a> methods take parameters that specify pins by index number. For these methods, output pins and input pins are both indexed from zero. Use the <code>get_PinCounts</code> method to determine the upper bounds for each.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamcrossbar">IAMCrossbar Interface</a>



<a href="/windows/desktop/DirectShow/working-with-crossbars">Working with Crossbars</a>