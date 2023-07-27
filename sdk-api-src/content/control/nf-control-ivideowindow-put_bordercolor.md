---
UID: NF:control.IVideoWindow.put_BorderColor
title: IVideoWindow::put_BorderColor (control.h)
description: The put_BorderColor method sets the color that appears around the edges of the destination rectangle.
helpviewer_keywords: ["IVideoWindow interface [DirectShow]","put_BorderColor method","IVideoWindow.put_BorderColor","IVideoWindow::put_BorderColor","IVideoWindowput_BorderColor","control/IVideoWindow::put_BorderColor","dshow.ivideowindow_put_bordercolor","put_BorderColor","put_BorderColor method [DirectShow]","put_BorderColor method [DirectShow]","IVideoWindow interface"]
old-location: dshow\ivideowindow_put_bordercolor.htm
tech.root: dshow
ms.assetid: c0e249f4-4a17-4c5d-8f16-bb1aceef2064
ms.date: 4/26/2023
ms.keywords: IVideoWindow interface [DirectShow],put_BorderColor method, IVideoWindow.put_BorderColor, IVideoWindow::put_BorderColor, IVideoWindowput_BorderColor, control/IVideoWindow::put_BorderColor, dshow.ivideowindow_put_bordercolor, put_BorderColor, put_BorderColor method [DirectShow], put_BorderColor method [DirectShow],IVideoWindow interface
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
 - IVideoWindow::put_BorderColor
 - control/IVideoWindow::put_BorderColor
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
 - IVideoWindow.put_BorderColor
---

# IVideoWindow::put_BorderColor


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_BorderColor</code> method sets the color that appears around the edges of the destination rectangle.

## -parameters

### -param Color [in]

The border color, specified as a <b>COLORREF</b> value.

## -returns

Possible return values include the following:

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
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The video renderer filter is not connected.

</td>
</tr>
</table>

## -remarks

If the destination rectangle is smaller than the client area of the video window, a border is exposed around the edges of the video. The default color is black. Use this method to override the default color. If a palette is in use, a nonsystem color is converted to its closest match.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nf-control-ibasicvideo-setdestinationposition">IBasicVideo::SetDestinationPosition</a>



<a href="/windows/desktop/api/control/nn-control-ivideowindow">IVideoWindow Interface</a>



<a href="/windows/desktop/api/control/nf-control-ivideowindow-get_bordercolor">IVideoWindow::get_BorderColor</a>