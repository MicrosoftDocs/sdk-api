---
UID: NF:strmif.IAMExtTransport.get_LocalControl
title: IAMExtTransport::get_LocalControl (strmif.h)
description: The get_LocalControl method determines whether the transport is under local control or remote control.
helpviewer_keywords: ["IAMExtTransport interface [DirectShow]","get_LocalControl method","IAMExtTransport.get_LocalControl","IAMExtTransport::get_LocalControl","IAMExtTransportget_LocalControl","dshow.iamexttransport_get_localcontrol","get_LocalControl","get_LocalControl method [DirectShow]","get_LocalControl method [DirectShow]","IAMExtTransport interface","strmif/IAMExtTransport::get_LocalControl"]
old-location: dshow\iamexttransport_get_localcontrol.htm
tech.root: dshow
ms.assetid: 793078a2-bddd-469b-9043-f07830499353
ms.date: 4/26/2023
ms.keywords: IAMExtTransport interface [DirectShow],get_LocalControl method, IAMExtTransport.get_LocalControl, IAMExtTransport::get_LocalControl, IAMExtTransportget_LocalControl, dshow.iamexttransport_get_localcontrol, get_LocalControl, get_LocalControl method [DirectShow], get_LocalControl method [DirectShow],IAMExtTransport interface, strmif/IAMExtTransport::get_LocalControl
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
 - IAMExtTransport::get_LocalControl
 - strmif/IAMExtTransport::get_LocalControl
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
 - IAMExtTransport.get_LocalControl
---

# IAMExtTransport::get_LocalControl


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_LocalControl</code> method determines whether the transport is under local control or remote control.



This method is not implemented.

## -parameters

### -param pState [out]

Pointer to a <b>long</b> integer that receives one of the following values:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>OATRUE</td>
<td>Local control.</td>
</tr>
<tr>
<td>OAFALSE</td>
<td>Remote control.</td>
</tr>
</table>

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -remarks

To control an external device from an application, the device must be in remote mode.

<h3><a id="DV_Implementation"></a><a id="dv_implementation"></a><a id="DV_IMPLEMENTATION"></a>DV Implementation</h3>

<a href="/windows/desktop/DirectShow/msdv-driver">MSDV</a> does not support this method. It returns E_NOTIMPL.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-put_localcontrol">IAMExtTransport::put_LocalControl</a>