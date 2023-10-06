---
UID: NF:control.IVideoWindow.HideCursor
title: IVideoWindow::HideCursor (control.h)
description: The HideCursor method shows or hides the cursor when the mouse is positioned over the video window.
helpviewer_keywords: ["HideCursor","HideCursor method [DirectShow]","HideCursor method [DirectShow]","IVideoWindow interface","IVideoWindow interface [DirectShow]","HideCursor method","IVideoWindow.HideCursor","IVideoWindow::HideCursor","IVideoWindowHideCursor","OAFALSE","OATRUE","control/IVideoWindow::HideCursor","dshow.ivideowindow_hidecursor"]
old-location: dshow\ivideowindow_hidecursor.htm
tech.root: dshow
ms.assetid: c45da114-6711-427b-8533-4ed339a42ff4
ms.date: 4/26/2023
ms.keywords: HideCursor, HideCursor method [DirectShow], HideCursor method [DirectShow],IVideoWindow interface, IVideoWindow interface [DirectShow],HideCursor method, IVideoWindow.HideCursor, IVideoWindow::HideCursor, IVideoWindowHideCursor, OAFALSE, OATRUE, control/IVideoWindow::HideCursor, dshow.ivideowindow_hidecursor
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
 - IVideoWindow::HideCursor
 - control/IVideoWindow::HideCursor
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
 - IVideoWindow.HideCursor
---

# IVideoWindow::HideCursor


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>HideCursor</code> method shows or hides the cursor when the mouse is positioned over the video window.

## -parameters

### -param HideCursor [in]

Specifies whether to show or hide the cursor. Must be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OATRUE"></a><a id="oatrue"></a><dl>
<dt><b>OATRUE</b></dt>
</dl>
</td>
<td width="60%">
Hide the cursor.

</td>
</tr>
<tr>
<td width="40%"><a id="OAFALSE"></a><a id="oafalse"></a><dl>
<dt><b>OAFALSE</b></dt>
</dl>
</td>
<td width="60%">
Show the cursor.

</td>
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



<a href="/windows/desktop/api/control/nf-control-ivideowindow-iscursorhidden">IVideoWindow::IsCursorHidden</a>