---
UID: NF:amvideo.IFullScreenVideoEx.GetMessageDrain
title: IFullScreenVideoEx::GetMessageDrain (amvideo.h)
description: The GetMessageDrain method retrieves the window that receives mouse and keyboard messages, if any.
helpviewer_keywords: ["GetMessageDrain","GetMessageDrain method [DirectShow]","GetMessageDrain method [DirectShow]","IFullScreenVideoEx interface","IFullScreenVideoEx interface [DirectShow]","GetMessageDrain method","IFullScreenVideoEx.GetMessageDrain","IFullScreenVideoEx::GetMessageDrain","IFullScreenVideoGetMessageDrain","amvideo/IFullScreenVideoEx::GetMessageDrain","dshow.ifullscreenvideoex_getmessagedrain"]
old-location: dshow\ifullscreenvideoex_getmessagedrain.htm
tech.root: dshow
ms.assetid: c1a83ad9-be4b-4adf-a316-d5dfb3df05ef
ms.date: 4/26/2023
ms.keywords: GetMessageDrain, GetMessageDrain method [DirectShow], GetMessageDrain method [DirectShow],IFullScreenVideoEx interface, IFullScreenVideoEx interface [DirectShow],GetMessageDrain method, IFullScreenVideoEx.GetMessageDrain, IFullScreenVideoEx::GetMessageDrain, IFullScreenVideoGetMessageDrain, amvideo/IFullScreenVideoEx::GetMessageDrain, dshow.ifullscreenvideoex_getmessagedrain
req.header: amvideo.h
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
 - IFullScreenVideoEx::GetMessageDrain
 - amvideo/IFullScreenVideoEx::GetMessageDrain
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
 - IFullScreenVideoEx.GetMessageDrain
---

# IFullScreenVideoEx::GetMessageDrain


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetMessageDrain</code> method retrieves the window that receives mouse and keyboard messages, if any.

## -parameters

### -param hwnd [out]

Pointer to a variable that receives the handle of the window. If no window has been designated to receive messages, this parameter receives the value <b>NULL</b>.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

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
<b>NULL</b> pointer argument.

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
</table>

## -remarks

This method is equivalent to the <a href="/windows/desktop/api/control/nf-control-ivideowindow-get_messagedrain">IVideoWindow::get_MessageDrain</a> method.

The Full Screen video renderer posts all mouse and keyboard messages to the window designated as a message drain. The exact list of messages that are posted is the same as the list given in <a href="/windows/desktop/api/control/nf-control-ivideowindow-put_messagedrain">IVideoWindow::put_MessageDrain</a>.

Applications do not need to use this method. Use the <a href="/windows/desktop/api/control/nf-control-ivideowindow-get_messagedrain">IVideoWindow::get_MessageDrain</a> method on the Filter Graph Manager instead.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-ifullscreenvideoex">IFullScreenVideoEx Interface</a>