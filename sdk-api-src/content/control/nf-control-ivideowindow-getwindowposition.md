---
UID: NF:control.IVideoWindow.GetWindowPosition
title: IVideoWindow::GetWindowPosition (control.h)
description: The GetWindowPosition method retrieves the position of the video window.
helpviewer_keywords: ["GetWindowPosition","GetWindowPosition method [DirectShow]","GetWindowPosition method [DirectShow]","IVideoWindow interface","IVideoWindow interface [DirectShow]","GetWindowPosition method","IVideoWindow.GetWindowPosition","IVideoWindow::GetWindowPosition","IVideoWindowGetWindowPosition","control/IVideoWindow::GetWindowPosition","dshow.ivideowindow_getwindowposition"]
old-location: dshow\ivideowindow_getwindowposition.htm
tech.root: dshow
ms.assetid: df55c10d-aec1-42f3-8bfb-207ae8804e72
ms.date: 4/26/2023
ms.keywords: GetWindowPosition, GetWindowPosition method [DirectShow], GetWindowPosition method [DirectShow],IVideoWindow interface, IVideoWindow interface [DirectShow],GetWindowPosition method, IVideoWindow.GetWindowPosition, IVideoWindow::GetWindowPosition, IVideoWindowGetWindowPosition, control/IVideoWindow::GetWindowPosition, dshow.ivideowindow_getwindowposition
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
 - IVideoWindow::GetWindowPosition
 - control/IVideoWindow::GetWindowPosition
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
 - IVideoWindow.GetWindowPosition
---

# IVideoWindow::GetWindowPosition


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetWindowPosition</code> method retrieves the position of the video window.

## -parameters

### -param pLeft [out]

Receives the x-coordinate, in pixels.

### -param pTop [out]

Receives the y-coordinate, in pixels.

### -param pWidth [out]

Receives the width of the window, in pixels.

### -param pHeight [out]

Receives the height of the window, in pixels.

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

## -remarks

This method has the same effect as calling the <a href="/windows/desktop/api/control/nf-control-ivideowindow-get_left">IVideoWindow::get_Left</a>, <a href="/windows/desktop/api/control/nf-control-ivideowindow-get_top">IVideoWindow::get_Top</a>, <a href="/windows/desktop/api/control/nf-control-ivideowindow-get_width">IVideoWindow::get_Width</a>, and <a href="/windows/desktop/api/control/nf-control-ivideowindow-get_height">IVideoWindow::get_Height</a> methods.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ivideowindow">IVideoWindow Interface</a>



<a href="/windows/desktop/api/control/nf-control-ivideowindow-setwindowposition">IVideoWindow::SetWindowPosition</a>