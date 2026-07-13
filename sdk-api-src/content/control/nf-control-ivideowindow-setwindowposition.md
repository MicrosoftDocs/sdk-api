---
UID: NF:control.IVideoWindow.SetWindowPosition
title: IVideoWindow::SetWindowPosition (control.h)
description: The SetWindowPosition method sets the position of the video window.
helpviewer_keywords: ["IVideoWindow interface [DirectShow]","SetWindowPosition method","IVideoWindow.SetWindowPosition","IVideoWindow::SetWindowPosition","IVideoWindowSetWindowPosition","SetWindowPosition","SetWindowPosition method [DirectShow]","SetWindowPosition method [DirectShow]","IVideoWindow interface","control/IVideoWindow::SetWindowPosition","dshow.ivideowindow_setwindowposition"]
old-location: dshow\ivideowindow_setwindowposition.htm
tech.root: dshow
ms.assetid: 5e667044-1781-4380-b855-d15cf8cd2349
ms.date: 4/26/2023
ms.keywords: IVideoWindow interface [DirectShow],SetWindowPosition method, IVideoWindow.SetWindowPosition, IVideoWindow::SetWindowPosition, IVideoWindowSetWindowPosition, SetWindowPosition, SetWindowPosition method [DirectShow], SetWindowPosition method [DirectShow],IVideoWindow interface, control/IVideoWindow::SetWindowPosition, dshow.ivideowindow_setwindowposition
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
 - IVideoWindow::SetWindowPosition
 - control/IVideoWindow::SetWindowPosition
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
 - IVideoWindow.SetWindowPosition
---

# IVideoWindow::SetWindowPosition


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetWindowPosition</code> method sets the position of the video window.

## -parameters

### -param Left [in]

The x-coordinate, in pixels.

### -param Top [in]

The y-coordinate, in pixels.

### -param Width [in]

The width, in pixels.

### -param Height [in]

The height, in pixels.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

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

This method has the same effect as calling the <a href="/windows/desktop/api/control/nf-control-ivideowindow-put_left">IVideoWindow::put_Left</a>, <a href="/windows/desktop/api/control/nf-control-ivideowindow-put_top">IVideoWindow::put_Top</a>, <a href="/windows/desktop/api/control/nf-control-ivideowindow-put_width">IVideoWindow::put_Width</a>, and <a href="/windows/desktop/api/control/nf-control-ivideowindow-put_height">IVideoWindow::put_Height</a> methods.

If resizing the window to the specified dimensions is impossible, this method modifies the window's size and location to make the window fit. Call the <a href="/windows/desktop/api/control/nf-control-ivideowindow-getwindowposition">IVideoWindow::GetWindowPosition</a> method to determine the result.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ivideowindow">IVideoWindow Interface</a>