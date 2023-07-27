---
UID: NF:amvideo.IFullScreenVideoEx.IsHideOnDeactivate
title: IFullScreenVideoEx::IsHideOnDeactivate (amvideo.h)
description: The IsHideOnDeactivate method indicates the behavior when the user switches to another application.
helpviewer_keywords: ["IFullScreenVideoEx interface [DirectShow]","IsHideOnDeactivate method","IFullScreenVideoEx.IsHideOnDeactivate","IFullScreenVideoEx::IsHideOnDeactivate","IFullScreenVideoIsHideOnDeactivate","IsHideOnDeactivate","IsHideOnDeactivate method [DirectShow]","IsHideOnDeactivate method [DirectShow]","IFullScreenVideoEx interface","amvideo/IFullScreenVideoEx::IsHideOnDeactivate","dshow.ifullscreenvideoex_ishideondeactivate"]
old-location: dshow\ifullscreenvideoex_ishideondeactivate.htm
tech.root: dshow
ms.assetid: 0196215f-4efe-418a-acf3-445b8224a2ab
ms.date: 4/26/2023
ms.keywords: IFullScreenVideoEx interface [DirectShow],IsHideOnDeactivate method, IFullScreenVideoEx.IsHideOnDeactivate, IFullScreenVideoEx::IsHideOnDeactivate, IFullScreenVideoIsHideOnDeactivate, IsHideOnDeactivate, IsHideOnDeactivate method [DirectShow], IsHideOnDeactivate method [DirectShow],IFullScreenVideoEx interface, amvideo/IFullScreenVideoEx::IsHideOnDeactivate, dshow.ifullscreenvideoex_ishideondeactivate
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
 - IFullScreenVideoEx::IsHideOnDeactivate
 - amvideo/IFullScreenVideoEx::IsHideOnDeactivate
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
 - IFullScreenVideoEx.IsHideOnDeactivate
---

# IFullScreenVideoEx::IsHideOnDeactivate


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IsHideOnDeactivate</code> method indicates the behavior when the user switches to another application. Depending on the setting, the full-screen video window is either minimized or hidden. If it is minimized, it appears as an icon in the task bar; otherwise, it does not.



## -returns

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The video window is minimized. (Default)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The video window is hidden.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-ifullscreenvideoex">IFullScreenVideoEx Interface</a>
