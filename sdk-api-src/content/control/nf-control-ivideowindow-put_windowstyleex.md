---
UID: NF:control.IVideoWindow.put_WindowStyleEx
title: IVideoWindow::put_WindowStyleEx (control.h)
description: The put_WindowStyleEx method sets the extended window styles on the video window.
helpviewer_keywords: ["IVideoWindow interface [DirectShow]","put_WindowStyleEx method","IVideoWindow.put_WindowStyleEx","IVideoWindow::put_WindowStyleEx","IVideoWindowput_WindowStyleEx","control/IVideoWindow::put_WindowStyleEx","dshow.ivideowindow_put_windowstyleex","put_WindowStyleEx","put_WindowStyleEx method [DirectShow]","put_WindowStyleEx method [DirectShow]","IVideoWindow interface"]
old-location: dshow\ivideowindow_put_windowstyleex.htm
tech.root: dshow
ms.assetid: 19d56e9d-6f6d-46aa-b46f-a62302b41d2f
ms.date: 4/26/2023
ms.keywords: IVideoWindow interface [DirectShow],put_WindowStyleEx method, IVideoWindow.put_WindowStyleEx, IVideoWindow::put_WindowStyleEx, IVideoWindowput_WindowStyleEx, control/IVideoWindow::put_WindowStyleEx, dshow.ivideowindow_put_windowstyleex, put_WindowStyleEx, put_WindowStyleEx method [DirectShow], put_WindowStyleEx method [DirectShow],IVideoWindow interface
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
 - IVideoWindow::put_WindowStyleEx
 - control/IVideoWindow::put_WindowStyleEx
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
 - IVideoWindow.put_WindowStyleEx
---

# IVideoWindow::put_WindowStyleEx


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_WindowStyleEx</code> method sets the extended window styles on the video window.

## -parameters

### -param WindowStyleEx [in]

One or more flags from the GWL_EXSTYLE value of the Windows <b>SetWindowLong</b> function.

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

This method is a thin wrapper over the <b>SetWindowLong</b> function and must be treated with care. In particular, you should retrieve the current styles and then add or remove flags. With some exceptions, flags allowed by the Windows <b>CreateWindow</b> function are acceptable. However, do not use this method to change the window size.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ivideowindow">IVideoWindow Interface</a>



<a href="/windows/desktop/api/control/nf-control-ivideowindow-get_windowstyleex">IVideoWindow::get_WindowStyleEx</a>



<a href="/windows/desktop/api/control/nf-control-ivideowindow-put_windowstyle">IVideoWindow::put_WindowStyle</a>