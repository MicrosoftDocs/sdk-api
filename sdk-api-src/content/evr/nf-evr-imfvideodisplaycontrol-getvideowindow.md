---
UID: NF:evr.IMFVideoDisplayControl.GetVideoWindow
title: IMFVideoDisplayControl::GetVideoWindow (evr.h)
description: Gets the clipping window for the video.
helpviewer_keywords: ["0b2b6b61-a2c5-4efd-ac40-962b0c2ae9c5","GetVideoWindow","GetVideoWindow method [Media Foundation]","GetVideoWindow method [Media Foundation]","IMFVideoDisplayControl interface","IMFVideoDisplayControl interface [Media Foundation]","GetVideoWindow method","IMFVideoDisplayControl.GetVideoWindow","IMFVideoDisplayControl::GetVideoWindow","evr/IMFVideoDisplayControl::GetVideoWindow","mf.imfvideodisplaycontrol_getvideowindow"]
old-location: mf\imfvideodisplaycontrol_getvideowindow.htm
tech.root: mfarchive
ms.assetid: 0b2b6b61-a2c5-4efd-ac40-962b0c2ae9c5
ms.date: 12/05/2018
ms.keywords: 0b2b6b61-a2c5-4efd-ac40-962b0c2ae9c5, GetVideoWindow, GetVideoWindow method [Media Foundation], GetVideoWindow method [Media Foundation],IMFVideoDisplayControl interface, IMFVideoDisplayControl interface [Media Foundation],GetVideoWindow method, IMFVideoDisplayControl.GetVideoWindow, IMFVideoDisplayControl::GetVideoWindow, evr/IMFVideoDisplayControl::GetVideoWindow, mf.imfvideodisplaycontrol_getvideowindow
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
 - IMFVideoDisplayControl::GetVideoWindow
 - evr/IMFVideoDisplayControl::GetVideoWindow
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
 - IMFVideoDisplayControl.GetVideoWindow
archived: true
---

# IMFVideoDisplayControl::GetVideoWindow


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Gets the clipping window for the video.

## -parameters

### -param phwndVideo [out]

Receives a handle to the window where the enhanced video renderer (EVR) will draw the video.

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
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The video renderer has been shut down.

</td>
</tr>
</table>

## -remarks

There is no default clipping window. The application must set the clipping window.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol">IMFVideoDisplayControl</a>



<a href="/windows/desktop/medfound/using-the-video-display-controls">Using the Video Display Controls</a>