---
UID: NF:control.IVideoWindow.put_AutoShow
title: IVideoWindow::put_AutoShow (control.h)
description: The put_AutoShow method specifies whether the video renderer automatically shows the video window when it receives video data.
helpviewer_keywords: ["IVideoWindow interface [DirectShow]","put_AutoShow method","IVideoWindow.put_AutoShow","IVideoWindow::put_AutoShow","IVideoWindowput_AutoShow","control/IVideoWindow::put_AutoShow","dshow.ivideowindow_put_autoshow","put_AutoShow","put_AutoShow method [DirectShow]","put_AutoShow method [DirectShow]","IVideoWindow interface"]
old-location: dshow\ivideowindow_put_autoshow.htm
tech.root: dshow
ms.assetid: 7481a7e8-4b57-43cc-8304-b70616bbd532
ms.date: 4/26/2023
ms.keywords: IVideoWindow interface [DirectShow],put_AutoShow method, IVideoWindow.put_AutoShow, IVideoWindow::put_AutoShow, IVideoWindowput_AutoShow, control/IVideoWindow::put_AutoShow, dshow.ivideowindow_put_autoshow, put_AutoShow, put_AutoShow method [DirectShow], put_AutoShow method [DirectShow],IVideoWindow interface
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
 - IVideoWindow::put_AutoShow
 - control/IVideoWindow::put_AutoShow
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
 - IVideoWindow.put_AutoShow
---

# IVideoWindow::put_AutoShow


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_AutoShow</code> method specifies whether the video renderer automatically shows the video window when it receives video data.

## -parameters

### -param AutoShow [in]

Specifies whether the video renderer automatically shows the video window. Must be one of the following values:

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
<td>If the video renderer pauses or runs, it will automatically show the video window. (Default.)</td>
</tr>
<tr>
<td>OAFALSE
                </td>
<td>The video renderer will not automatically show the video window.</td>
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

## -remarks

By default, when the filter graph changes state to paused or running, the video renderer shows the video window and moves it to the foreground. If the user closes the window, it will not automatically reappear.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ivideowindow">IVideoWindow Interface</a>



<a href="/windows/desktop/api/control/nf-control-ivideowindow-get_autoshow">IVideoWindow::get_AutoShow</a>