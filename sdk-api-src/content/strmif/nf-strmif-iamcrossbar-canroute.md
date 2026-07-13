---
UID: NF:strmif.IAMCrossbar.CanRoute
title: IAMCrossbar::CanRoute (strmif.h)
description: The CanRoute method queries whether a specified input pin can be routed to a specified output pin.
helpviewer_keywords: ["CanRoute","CanRoute method [DirectShow]","CanRoute method [DirectShow]","IAMCrossbar interface","IAMCrossbar interface [DirectShow]","CanRoute method","IAMCrossbar.CanRoute","IAMCrossbar::CanRoute","IAMCrossbarCanRoute","dshow.iamcrossbar_canroute","strmif/IAMCrossbar::CanRoute"]
old-location: dshow\iamcrossbar_canroute.htm
tech.root: dshow
ms.assetid: 13be4b35-14d9-4565-8939-e6e755f256ab
ms.date: 4/26/2023
ms.keywords: CanRoute, CanRoute method [DirectShow], CanRoute method [DirectShow],IAMCrossbar interface, IAMCrossbar interface [DirectShow],CanRoute method, IAMCrossbar.CanRoute, IAMCrossbar::CanRoute, IAMCrossbarCanRoute, dshow.iamcrossbar_canroute, strmif/IAMCrossbar::CanRoute
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
 - IAMCrossbar::CanRoute
 - strmif/IAMCrossbar::CanRoute
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
 - IAMCrossbar.CanRoute
---

# IAMCrossbar::CanRoute


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>CanRoute</code> method queries whether a specified input pin can be routed to a specified output pin.

## -parameters

### -param OutputPinIndex [in]

Specifies the index of the output pin.

### -param InputPinIndex [in]

Specifies the index of input pin.

## -returns

Returns an <b>HRESULT</b> values. Possible values include the following.

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
These two pins can be routed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
These two pins cannot be routed.

</td>
</tr>
</table>

## -remarks

To route the pins, call the <a href="/windows/desktop/api/strmif/nf-strmif-iamcrossbar-route">IAMCrossbar::Route</a> method. Output pins and input pins are both indexed from zero. To determine the number of output and input pins, call the <a href="/windows/desktop/api/strmif/nf-strmif-iamcrossbar-get_pincounts">IAMCrossbar::get_PinCounts</a> method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamcrossbar">IAMCrossbar Interface</a>



<a href="/windows/desktop/DirectShow/working-with-crossbars">Working with Crossbars</a>