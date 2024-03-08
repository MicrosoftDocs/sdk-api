---
UID: NF:control.IVideoWindow.GetRestorePosition
title: IVideoWindow::GetRestorePosition (control.h)
description: The GetRestorePosition method retrieves the restored window position.
helpviewer_keywords: ["GetRestorePosition","GetRestorePosition method [DirectShow]","GetRestorePosition method [DirectShow]","IVideoWindow interface","IVideoWindow interface [DirectShow]","GetRestorePosition method","IVideoWindow.GetRestorePosition","IVideoWindow::GetRestorePosition","IVideoWindowGetRestorePosition","control/IVideoWindow::GetRestorePosition","dshow.ivideowindow_getrestoreposition"]
old-location: dshow\ivideowindow_getrestoreposition.htm
tech.root: dshow
ms.assetid: e2c8880a-e140-4bb1-8f0d-2d665c98728c
ms.date: 4/26/2023
ms.keywords: GetRestorePosition, GetRestorePosition method [DirectShow], GetRestorePosition method [DirectShow],IVideoWindow interface, IVideoWindow interface [DirectShow],GetRestorePosition method, IVideoWindow.GetRestorePosition, IVideoWindow::GetRestorePosition, IVideoWindowGetRestorePosition, control/IVideoWindow::GetRestorePosition, dshow.ivideowindow_getrestoreposition
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
 - IVideoWindow::GetRestorePosition
 - control/IVideoWindow::GetRestorePosition
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
 - IVideoWindow.GetRestorePosition
---

# IVideoWindow::GetRestorePosition


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetRestorePosition</code> method retrieves the restored window position.

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

If the video window is minimized or maximized, you can use this method to get the window's restored position.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ivideowindow">IVideoWindow Interface</a>