---
UID: NF:amvideo.IFullScreenVideoEx.HideOnDeactivate
title: IFullScreenVideoEx::HideOnDeactivate (amvideo.h)
description: The HideOnDeactivate method . Depending on the setting, the full-screen video window is either minimized or hidden. If it is minimized, it appears as an icon in the task bar; otherwise, it does not.
helpviewer_keywords: ["HideOnDeactivate","HideOnDeactivate method [DirectShow]","HideOnDeactivate method [DirectShow]","IFullScreenVideoEx interface","IFullScreenVideoEx interface [DirectShow]","HideOnDeactivate method","IFullScreenVideoEx.HideOnDeactivate","IFullScreenVideoEx::HideOnDeactivate","IFullScreenVideoHideOnDeactivate","amvideo/IFullScreenVideoEx::HideOnDeactivate","dshow.ifullscreenvideoex_hideondeactivate"]
old-location: dshow\ifullscreenvideoex_hideondeactivate.htm
tech.root: dshow
ms.assetid: b2839876-40b1-4b41-a3a4-99e5cbdd9ef1
ms.date: 4/26/2023
ms.keywords: HideOnDeactivate, HideOnDeactivate method [DirectShow], HideOnDeactivate method [DirectShow],IFullScreenVideoEx interface, IFullScreenVideoEx interface [DirectShow],HideOnDeactivate method, IFullScreenVideoEx.HideOnDeactivate, IFullScreenVideoEx::HideOnDeactivate, IFullScreenVideoHideOnDeactivate, amvideo/IFullScreenVideoEx::HideOnDeactivate, dshow.ifullscreenvideoex_hideondeactivate
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
 - IFullScreenVideoEx::HideOnDeactivate
 - amvideo/IFullScreenVideoEx::HideOnDeactivate
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
 - IFullScreenVideoEx.HideOnDeactivate
---

# IFullScreenVideoEx::HideOnDeactivate


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>HideOnDeactivate</code> method . Depending on the setting, the full-screen video window is either minimized or hidden. If it is minimized, it appears as an icon in the task bar; otherwise, it does not.

## -parameters

### -param Hide [in]

Value that specifies the behavior when the application is deactivated. Set to OATRUE to hide the icon; set to OAFALSE to display the icon.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>OATRUE</td>
<td>Hide the video window.</td>
</tr>
<tr>
<td>OAFALSE</td>
<td>Minimize the video window. (Default)</td>
</tr>
</table>

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