---
UID: NF:strmif.IPin.QueryDirection
title: IPin::QueryDirection (strmif.h)
description: The QueryDirection method gets the direction of the pin (input or output).
helpviewer_keywords: ["IPin interface [DirectShow]","QueryDirection method","IPin.QueryDirection","IPin::QueryDirection","IPinQueryDirection","QueryDirection","QueryDirection method [DirectShow]","QueryDirection method [DirectShow]","IPin interface","dshow.ipin_querydirection","strmif/IPin::QueryDirection"]
old-location: dshow\ipin_querydirection.htm
tech.root: dshow
ms.assetid: cc36b5d6-bcca-403d-b840-ceabbf159f5d
ms.date: 4/26/2023
ms.keywords: IPin interface [DirectShow],QueryDirection method, IPin.QueryDirection, IPin::QueryDirection, IPinQueryDirection, QueryDirection, QueryDirection method [DirectShow], QueryDirection method [DirectShow],IPin interface, dshow.ipin_querydirection, strmif/IPin::QueryDirection
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
 - IPin::QueryDirection
 - strmif/IPin::QueryDirection
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
 - IPin.QueryDirection
---

# IPin::QueryDirection


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>QueryDirection</b> method gets the direction of the pin (input or output).

## -parameters

### -param pPinDir [out]

Receives a member of the [PIN_DIRECTION](/windows/desktop/api/strmif/ne-strmif-pin_direction) enumerated type.

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

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin Interface</a>