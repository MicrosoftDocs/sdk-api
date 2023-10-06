---
UID: NF:control.IVideoWindow.put_MessageDrain
title: IVideoWindow::put_MessageDrain (control.h)
description: The put_MessageDrain method specifies a window to receive mouse and keyboard messages from the video window.
helpviewer_keywords: ["IVideoWindow interface [DirectShow]","put_MessageDrain method","IVideoWindow.put_MessageDrain","IVideoWindow::put_MessageDrain","IVideoWindowput_MessageDrain","control/IVideoWindow::put_MessageDrain","dshow.ivideowindow_put_messagedrain","put_MessageDrain","put_MessageDrain method [DirectShow]","put_MessageDrain method [DirectShow]","IVideoWindow interface"]
old-location: dshow\ivideowindow_put_messagedrain.htm
tech.root: dshow
ms.assetid: aaf8624c-b3ea-4034-845a-6cd74c725c44
ms.date: 4/26/2023
ms.keywords: IVideoWindow interface [DirectShow],put_MessageDrain method, IVideoWindow.put_MessageDrain, IVideoWindow::put_MessageDrain, IVideoWindowput_MessageDrain, control/IVideoWindow::put_MessageDrain, dshow.ivideowindow_put_messagedrain, put_MessageDrain, put_MessageDrain method [DirectShow], put_MessageDrain method [DirectShow],IVideoWindow interface
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
 - IVideoWindow::put_MessageDrain
 - control/IVideoWindow::put_MessageDrain
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
 - IVideoWindow.put_MessageDrain
---

# IVideoWindow::put_MessageDrain


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_MessageDrain</code> method specifies a window to receive mouse and keyboard messages from the video window.

## -parameters

### -param Drain [in]

A handle to the window, as an <a href="/windows/desktop/DirectShow/oahwnd">OAHWND</a> value.

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

This method enables an application to respond to mouse and keyboard events generated within the video window.

If <i>Drain</i> is non-<b>NULL</b>, the video renderer forwards certain messages to the specified window, using the <b>PostMessage</b> function. Which messages are forwarded might depend on the video renderer in use. The <a href="/windows/desktop/DirectShow/video-renderer-filter">Video Renderer</a> and Video Mixing Renderer (VMR) filters forward the following messages:

<ul>
<li>WM_CHAR</li>
<li>WM_DEADCHAR</li>
<li>WM_KEYDOWN</li>
<li>WM_KEYUP</li>
<li>WM_LBUTTONDBLCLK</li>
<li>WM_LBUTTONDOWN</li>
<li>WM_LBUTTONUP</li>
<li>WM_MBUTTONDBLCLK</li>
<li>WM_MBUTTONDOWN</li>
<li>WM_MBUTTONUP</li>
<li>WM_MOUSEACTIVATE</li>
<li>WM_MOUSEMOVE</li>
<li>WM_NCLBUTTONDBLCLK</li>
<li>WM_NCLBUTTONDOWN</li>
<li>WM_NCLBUTTONUP</li>
<li>WM_NCMBUTTONDBLCLK</li>
<li>WM_NCMBUTTONDOWN</li>
<li>WM_NCMBUTTONUP</li>
<li>WM_NCMOUSEMOVE</li>
<li>WM_NCRBUTTONDBLCLK</li>
<li>WM_NCRBUTTONDOWN</li>
<li>WM_NCRBUTTONUP</li>
<li>WM_RBUTTONDBLCLK</li>
<li>WM_RBUTTONDOWN</li>
<li>WM_RBUTTONUP</li>
<li>WM_SYSCHAR</li>
<li>WM_SYSDEADCHAR</li>
<li>WM_SYSKEYDOWN</li>
<li>WM_SYSKEYUP</li>
</ul>
The message drain window does not need to be a parent of the video window, so full-screen applications can use this method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ivideowindow">IVideoWindow Interface</a>



<a href="/windows/desktop/api/control/nf-control-ivideowindow-get_messagedrain">IVideoWindow::get_MessageDrain</a>