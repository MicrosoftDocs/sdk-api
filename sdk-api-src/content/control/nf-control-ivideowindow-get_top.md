---
UID: NF:control.IVideoWindow.get_Top
title: IVideoWindow::get_Top (control.h)
description: The get_Top method retrieves the video window's y-coordinate.
helpviewer_keywords: ["IVideoWindow interface [DirectShow]","get_Top method","IVideoWindow.get_Top","IVideoWindow::get_Top","IVideoWindowget_Top","control/IVideoWindow::get_Top","dshow.ivideowindow_get_top","get_Top","get_Top method [DirectShow]","get_Top method [DirectShow]","IVideoWindow interface"]
old-location: dshow\ivideowindow_get_top.htm
tech.root: dshow
ms.assetid: 00baab45-d740-4f74-bd53-eb2ff21c5dcc
ms.date: 4/26/2023
ms.keywords: IVideoWindow interface [DirectShow],get_Top method, IVideoWindow.get_Top, IVideoWindow::get_Top, IVideoWindowget_Top, control/IVideoWindow::get_Top, dshow.ivideowindow_get_top, get_Top, get_Top method [DirectShow], get_Top method [DirectShow],IVideoWindow interface
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
 - IVideoWindow::get_Top
 - control/IVideoWindow::get_Top
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
 - IVideoWindow.get_Top
---

# IVideoWindow::get_Top


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_Top</code> method retrieves the video window's y-coordinate.

## -parameters

### -param pTop [out]

Receives the y-coordinate, in pixels.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer.

</td>
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

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ivideowindow">IVideoWindow Interface</a>



<a href="/windows/desktop/api/control/nf-control-ivideowindow-put_top">IVideoWindow::put_Top</a>