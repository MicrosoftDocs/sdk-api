---
UID: NF:control.IVideoWindow.SetWindowForeground
title: IVideoWindow::SetWindowForeground (control.h)
description: The SetWindowForeground method places the video window at the top of the Z order.
helpviewer_keywords: ["IVideoWindow interface [DirectShow]","SetWindowForeground method","IVideoWindow.SetWindowForeground","IVideoWindow::SetWindowForeground","IVideoWindowSetWindowForeground","SetWindowForeground","SetWindowForeground method [DirectShow]","SetWindowForeground method [DirectShow]","IVideoWindow interface","control/IVideoWindow::SetWindowForeground","dshow.ivideowindow_setwindowforeground"]
old-location: dshow\ivideowindow_setwindowforeground.htm
tech.root: dshow
ms.assetid: ff4f3707-1f2e-499b-8108-81616fe4ae9b
ms.date: 4/26/2023
ms.keywords: IVideoWindow interface [DirectShow],SetWindowForeground method, IVideoWindow.SetWindowForeground, IVideoWindow::SetWindowForeground, IVideoWindowSetWindowForeground, SetWindowForeground, SetWindowForeground method [DirectShow], SetWindowForeground method [DirectShow],IVideoWindow interface, control/IVideoWindow::SetWindowForeground, dshow.ivideowindow_setwindowforeground
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
 - IVideoWindow::SetWindowForeground
 - control/IVideoWindow::SetWindowForeground
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
 - IVideoWindow.SetWindowForeground
---

# IVideoWindow::SetWindowForeground


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetWindowForeground</code> method places the video window at the top of the Z order.

## -parameters

### -param Focus

Specifies whether to give the window focus. Must be one of the following values:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>OATRUE
                </td>
<td>Give the window focus.</td>
</tr>
<tr>
<td>OAFALSE
                </td>
<td>Do not give the window focus.</td>
</tr>
</table>

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

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ivideowindow">IVideoWindow Interface</a>