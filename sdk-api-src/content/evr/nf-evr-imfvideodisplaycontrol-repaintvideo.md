---
UID: NF:evr.IMFVideoDisplayControl.RepaintVideo
title: IMFVideoDisplayControl::RepaintVideo (evr.h)
description: Repaints the current video frame. Call this method whenever the application receives a WM_PAINT message.
helpviewer_keywords: ["IMFVideoDisplayControl interface [Media Foundation]","RepaintVideo method","IMFVideoDisplayControl.RepaintVideo","IMFVideoDisplayControl::RepaintVideo","RepaintVideo","RepaintVideo method [Media Foundation]","RepaintVideo method [Media Foundation]","IMFVideoDisplayControl interface","c8051883-2a48-4ca4-a7d2-c90d0d451cd2","evr/IMFVideoDisplayControl::RepaintVideo","mf.imfvideodisplaycontrol_repaintvideo"]
old-location: mf\imfvideodisplaycontrol_repaintvideo.htm
tech.root: mfarchive
ms.assetid: c8051883-2a48-4ca4-a7d2-c90d0d451cd2
ms.date: 12/05/2018
ms.keywords: IMFVideoDisplayControl interface [Media Foundation],RepaintVideo method, IMFVideoDisplayControl.RepaintVideo, IMFVideoDisplayControl::RepaintVideo, RepaintVideo, RepaintVideo method [Media Foundation], RepaintVideo method [Media Foundation],IMFVideoDisplayControl interface, c8051883-2a48-4ca4-a7d2-c90d0d451cd2, evr/IMFVideoDisplayControl::RepaintVideo, mf.imfvideodisplaycontrol_repaintvideo
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IMFVideoDisplayControl::RepaintVideo
 - evr/IMFVideoDisplayControl::RepaintVideo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoDisplayControl.RepaintVideo
archived: true
---

# IMFVideoDisplayControl::RepaintVideo


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Repaints the current video frame. Call this method whenever the application receives a WM_PAINT message.



## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The EVR cannot repaint the frame at this time. This error can occur while the EVR is switching between full-screen and windowed mode. The caller can safely ignore this error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The video renderer has been shut down.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol">IMFVideoDisplayControl</a>



<a href="/windows/desktop/medfound/using-the-video-display-controls">Using the Video Display Controls</a>
