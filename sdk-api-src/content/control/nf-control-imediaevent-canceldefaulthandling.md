---
UID: NF:control.IMediaEvent.CancelDefaultHandling
title: IMediaEvent::CancelDefaultHandling (control.h)
description: The CancelDefaultHandling method cancels the Filter Graph Manager's default handling for a specified event. The event notification is passed to the application.
helpviewer_keywords: ["CancelDefaultHandling","CancelDefaultHandling method [DirectShow]","CancelDefaultHandling method [DirectShow]","IMediaEvent interface","IMediaEvent interface [DirectShow]","CancelDefaultHandling method","IMediaEvent.CancelDefaultHandling","IMediaEvent::CancelDefaultHandling","IMediaEventCancelDefaultHandling","control/IMediaEvent::CancelDefaultHandling","dshow.imediaevent_canceldefaulthandling"]
old-location: dshow\imediaevent_canceldefaulthandling.htm
tech.root: dshow
ms.assetid: 955d0494-8418-42a1-ab6e-2c779165f578
ms.date: 4/26/2023
ms.keywords: CancelDefaultHandling, CancelDefaultHandling method [DirectShow], CancelDefaultHandling method [DirectShow],IMediaEvent interface, IMediaEvent interface [DirectShow],CancelDefaultHandling method, IMediaEvent.CancelDefaultHandling, IMediaEvent::CancelDefaultHandling, IMediaEventCancelDefaultHandling, control/IMediaEvent::CancelDefaultHandling, dshow.imediaevent_canceldefaulthandling
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
 - IMediaEvent::CancelDefaultHandling
 - control/IMediaEvent::CancelDefaultHandling
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
 - IMediaEvent.CancelDefaultHandling
---

# IMediaEvent::CancelDefaultHandling


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>CancelDefaultHandling</code> method cancels the Filter Graph Manager's default handling for a specified event. The event notification is passed to the application.

## -parameters

### -param lEvCode

Event code for which to cancel default handling.

## -returns

Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
No default handling for this event.

</td>
</tr>
</table>

## -remarks

To restore the default handling for an event, call the <a href="/windows/desktop/api/control/nf-control-imediaevent-restoredefaulthandling">IMediaEvent::RestoreDefaultHandling</a> method with the event code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-imediaevent">IMediaEvent Interface</a>