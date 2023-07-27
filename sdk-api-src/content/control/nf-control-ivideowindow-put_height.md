---
UID: NF:control.IVideoWindow.put_Height
title: IVideoWindow::put_Height (control.h)
description: The put_Height method sets the height of the video window.
helpviewer_keywords: ["IVideoWindow interface [DirectShow]","put_Height method","IVideoWindow.put_Height","IVideoWindow::put_Height","IVideoWindowput_Height","control/IVideoWindow::put_Height","dshow.ivideowindow_put_height","put_Height","put_Height method [DirectShow]","put_Height method [DirectShow]","IVideoWindow interface"]
old-location: dshow\ivideowindow_put_height.htm
tech.root: dshow
ms.assetid: 39ba411f-675f-4dad-be4f-6beffbd3b53c
ms.date: 4/26/2023
ms.keywords: IVideoWindow interface [DirectShow],put_Height method, IVideoWindow.put_Height, IVideoWindow::put_Height, IVideoWindowput_Height, control/IVideoWindow::put_Height, dshow.ivideowindow_put_height, put_Height, put_Height method [DirectShow], put_Height method [DirectShow],IVideoWindow interface
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
 - IVideoWindow::put_Height
 - control/IVideoWindow::put_Height
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
 - IVideoWindow.put_Height
---

# IVideoWindow::put_Height


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_Height</code> method sets the height of the video window.

## -parameters

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

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ivideowindow">IVideoWindow Interface</a>



<a href="/windows/desktop/api/control/nf-control-ivideowindow-get_height">IVideoWindow::get_Height</a>