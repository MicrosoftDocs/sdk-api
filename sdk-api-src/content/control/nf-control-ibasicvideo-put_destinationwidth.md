---
UID: NF:control.IBasicVideo.put_DestinationWidth
title: IBasicVideo::put_DestinationWidth (control.h)
description: The put_DestinationWidth method sets the width of the destination rectangle.
helpviewer_keywords: ["IBasicVideo interface [DirectShow]","put_DestinationWidth method","IBasicVideo.put_DestinationWidth","IBasicVideo::put_DestinationWidth","IBasicVideoput_DestinationWidth","control/IBasicVideo::put_DestinationWidth","dshow.ibasicvideo_put_destinationwidth","put_DestinationWidth","put_DestinationWidth method [DirectShow]","put_DestinationWidth method [DirectShow]","IBasicVideo interface"]
old-location: dshow\ibasicvideo_put_destinationwidth.htm
tech.root: dshow
ms.assetid: 4ae22194-19ca-4a20-9b4f-d9f39e346606
ms.date: 4/26/2023
ms.keywords: IBasicVideo interface [DirectShow],put_DestinationWidth method, IBasicVideo.put_DestinationWidth, IBasicVideo::put_DestinationWidth, IBasicVideoput_DestinationWidth, control/IBasicVideo::put_DestinationWidth, dshow.ibasicvideo_put_destinationwidth, put_DestinationWidth, put_DestinationWidth method [DirectShow], put_DestinationWidth method [DirectShow],IBasicVideo interface
req.header: control.h
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
 - IBasicVideo::put_DestinationWidth
 - control/IBasicVideo::put_DestinationWidth
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
 - IBasicVideo.put_DestinationWidth
---

# IBasicVideo::put_DestinationWidth


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_DestinationWidth</code> method sets the width of the destination rectangle.

## -parameters

### -param DestinationWidth [in]

Specifies the width, in pixels.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument. <i>DestinationWidth</i> must be larger than zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The video renderer is not connected.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ibasicvideo">IBasicVideo Interface</a>