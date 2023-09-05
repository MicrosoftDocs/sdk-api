---
UID: NF:amvideo.IFullScreenVideoEx.SetMonitor
title: IFullScreenVideoEx::SetMonitor (amvideo.h)
description: The SetMonitor method specifies which monitor to use. The Full Screen Renderer only supports the primary monitor, however, so this method is not useful in the current implementation.
helpviewer_keywords: ["IFullScreenVideoEx interface [DirectShow]","SetMonitor method","IFullScreenVideoEx.SetMonitor","IFullScreenVideoEx::SetMonitor","IFullScreenVideoSetMonitor","SetMonitor","SetMonitor method [DirectShow]","SetMonitor method [DirectShow]","IFullScreenVideoEx interface","amvideo/IFullScreenVideoEx::SetMonitor","dshow.ifullscreenvideoex_setmonitor"]
old-location: dshow\ifullscreenvideoex_setmonitor.htm
tech.root: dshow
ms.assetid: f2db1009-ce5b-4ebe-becb-bed3d1187335
ms.date: 4/26/2023
ms.keywords: IFullScreenVideoEx interface [DirectShow],SetMonitor method, IFullScreenVideoEx.SetMonitor, IFullScreenVideoEx::SetMonitor, IFullScreenVideoSetMonitor, SetMonitor, SetMonitor method [DirectShow], SetMonitor method [DirectShow],IFullScreenVideoEx interface, amvideo/IFullScreenVideoEx::SetMonitor, dshow.ifullscreenvideoex_setmonitor
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
 - IFullScreenVideoEx::SetMonitor
 - amvideo/IFullScreenVideoEx::SetMonitor
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
 - IFullScreenVideoEx.SetMonitor
---

# IFullScreenVideoEx::SetMonitor


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetMonitor</code> method specifies which monitor to use. The Full Screen Renderer only supports the primary monitor, however, so this method is not useful in the current implementation.

## -parameters

### -param Monitor [in]

Specifies the index of the monitor to use. Must be zero in the current implementation.

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
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-ifullscreenvideoex">IFullScreenVideoEx Interface</a>