---
UID: NF:strmif.IAMExtTransport.put_LocalControl
title: IAMExtTransport::put_LocalControl (strmif.h)
description: The put_LocalControl method switches the device between local and remote control.
helpviewer_keywords: ["IAMExtTransport interface [DirectShow]","put_LocalControl method","IAMExtTransport.put_LocalControl","IAMExtTransport::put_LocalControl","IAMExtTransportput_LocalControl","dshow.iamexttransport_put_localcontrol","put_LocalControl","put_LocalControl method [DirectShow]","put_LocalControl method [DirectShow]","IAMExtTransport interface","strmif/IAMExtTransport::put_LocalControl"]
old-location: dshow\iamexttransport_put_localcontrol.htm
tech.root: dshow
ms.assetid: 1ac75eb7-4b4c-402b-8e4e-f94488eccec1
ms.date: 4/26/2023
ms.keywords: IAMExtTransport interface [DirectShow],put_LocalControl method, IAMExtTransport.put_LocalControl, IAMExtTransport::put_LocalControl, IAMExtTransportput_LocalControl, dshow.iamexttransport_put_localcontrol, put_LocalControl, put_LocalControl method [DirectShow], put_LocalControl method [DirectShow],IAMExtTransport interface, strmif/IAMExtTransport::put_LocalControl
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
 - IAMExtTransport::put_LocalControl
 - strmif/IAMExtTransport::put_LocalControl
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
 - IAMExtTransport.put_LocalControl
---

# IAMExtTransport::put_LocalControl


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_LocalControl</code> method switches the device between local and remote control.



This method is not implemented.

## -parameters

### -param State [in]

Specifies the state of the device.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>OATRUE</td>
<td>Local control</td>
</tr>
<tr>
<td>OAFALSE</td>
<td>Remote control</td>
</tr>
</table>

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-get_localcontrol">IAMExtTransport::get_LocalControl</a>