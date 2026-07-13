---
UID: NF:control.IVideoWindow.put_WindowState
title: IVideoWindow::put_WindowState (control.h)
description: The put_WindowState method shows, hides, minimizes, or maximizes the video window.
helpviewer_keywords: ["IVideoWindow interface [DirectShow]","put_WindowState method","IVideoWindow.put_WindowState","IVideoWindow::put_WindowState","IVideoWindowput_WindowState","control/IVideoWindow::put_WindowState","dshow.ivideowindow_put_windowstate","put_WindowState","put_WindowState method [DirectShow]","put_WindowState method [DirectShow]","IVideoWindow interface"]
old-location: dshow\ivideowindow_put_windowstate.htm
tech.root: dshow
ms.assetid: 75189754-61c4-4196-9cfb-3f8c8e33efbc
ms.date: 4/26/2023
ms.keywords: IVideoWindow interface [DirectShow],put_WindowState method, IVideoWindow.put_WindowState, IVideoWindow::put_WindowState, IVideoWindowput_WindowState, control/IVideoWindow::put_WindowState, dshow.ivideowindow_put_windowstate, put_WindowState, put_WindowState method [DirectShow], put_WindowState method [DirectShow],IVideoWindow interface
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
 - IVideoWindow::put_WindowState
 - control/IVideoWindow::put_WindowState
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
 - IVideoWindow.put_WindowState
---

# IVideoWindow::put_WindowState


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_WindowState</code> method shows, hides, minimizes, or maximizes the video window.

## -parameters

### -param WindowState [in]

Flag that specifies how the window is to be shown. The value can be any constant defined for the <i>nCmdShow</i> parameter of the <a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a> function.

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

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ivideowindow">IVideoWindow Interface</a>



<a href="/windows/desktop/api/control/nf-control-ivideowindow-get_windowstate">IVideoWindow::get_WindowState</a>