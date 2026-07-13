---
UID: NF:control.IVideoWindow.put_Owner
title: IVideoWindow::put_Owner (control.h)
description: The put_Owner method specifies a parent window for the video window.
helpviewer_keywords: ["IVideoWindow interface [DirectShow]","put_Owner method","IVideoWindow.put_Owner","IVideoWindow::put_Owner","IVideoWindowput_Owner","control/IVideoWindow::put_Owner","dshow.ivideowindow_put_owner","put_Owner","put_Owner method [DirectShow]","put_Owner method [DirectShow]","IVideoWindow interface"]
old-location: dshow\ivideowindow_put_owner.htm
tech.root: dshow
ms.assetid: 658ad234-cb5a-428b-ae19-0cd52db6718b
ms.date: 4/26/2023
ms.keywords: IVideoWindow interface [DirectShow],put_Owner method, IVideoWindow.put_Owner, IVideoWindow::put_Owner, IVideoWindowput_Owner, control/IVideoWindow::put_Owner, dshow.ivideowindow_put_owner, put_Owner, put_Owner method [DirectShow], put_Owner method [DirectShow],IVideoWindow interface
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
 - IVideoWindow::put_Owner
 - control/IVideoWindow::put_Owner
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
 - IVideoWindow.put_Owner
---

# IVideoWindow::put_Owner


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_Owner</code> method specifies a parent window for the video window.

## -parameters

### -param Owner [in]

A handle to the parent window, as an <a href="/windows/desktop/DirectShow/oahwnd">OAHWND</a> value, or <b>NULL</b> to remove the existing parent.

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

Use this method to display videos in a compound document. This method changes the parent of the video window and sets the WS_CHILD style for the video window.

Reset the owner to <b>NULL</b> before releasing the Filter Graph Manager. Otherwise, messages will continue to be sent to this window and errors will likely occur when the application is terminated.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ivideowindow">IVideoWindow Interface</a>



<a href="/windows/desktop/api/control/nf-control-ivideowindow-get_owner">IVideoWindow::get_Owner</a>