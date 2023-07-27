---
UID: NF:control.IVideoWindow.get_Visible
title: IVideoWindow::get_Visible (control.h)
description: The get_Visible method queries whether the video window is visible.
helpviewer_keywords: ["IVideoWindow interface [DirectShow]","get_Visible method","IVideoWindow.get_Visible","IVideoWindow::get_Visible","IVideoWindowget_Visible","control/IVideoWindow::get_Visible","dshow.ivideowindow_get_visible","get_Visible","get_Visible method [DirectShow]","get_Visible method [DirectShow]","IVideoWindow interface"]
old-location: dshow\ivideowindow_get_visible.htm
tech.root: dshow
ms.assetid: b533398e-80f6-4f33-982b-93b8e0d705e9
ms.date: 4/26/2023
ms.keywords: IVideoWindow interface [DirectShow],get_Visible method, IVideoWindow.get_Visible, IVideoWindow::get_Visible, IVideoWindowget_Visible, control/IVideoWindow::get_Visible, dshow.ivideowindow_get_visible, get_Visible, get_Visible method [DirectShow], get_Visible method [DirectShow],IVideoWindow interface
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
 - IVideoWindow::get_Visible
 - control/IVideoWindow::get_Visible
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
 - IVideoWindow.get_Visible
---

# IVideoWindow::get_Visible


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_Visible</code> method queries whether the video window is visible.

## -parameters

### -param pVisible [out]

Receives the value OATRUE if the window is visible, or OAFALSE if the window is hidden.

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

This method checks for the WS_VISIBLE style bit, by calling the Windows <b>IsWindowVisible</b> method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ivideowindow">IVideoWindow Interface</a>



<a href="/windows/desktop/api/control/nf-control-ivideowindow-put_visible">IVideoWindow::put_Visible</a>