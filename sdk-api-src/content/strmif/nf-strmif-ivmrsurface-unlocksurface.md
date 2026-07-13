---
UID: NF:strmif.IVMRSurface.UnlockSurface
title: IVMRSurface::UnlockSurface (strmif.h)
description: The UnlockSurface method unlocks the attached DirectDraw surface.
helpviewer_keywords: ["IVMRSurface interface [DirectShow]","UnlockSurface method","IVMRSurface.UnlockSurface","IVMRSurface::UnlockSurface","IVMRSurfaceUnlockSurface","UnlockSurface","UnlockSurface method [DirectShow]","UnlockSurface method [DirectShow]","IVMRSurface interface","dshow.ivmrsurface_unlocksurface","strmif/IVMRSurface::UnlockSurface"]
old-location: dshow\ivmrsurface_unlocksurface.htm
tech.root: dshow
ms.assetid: f6acaf96-925c-46b9-8d56-11d94f3dbda3
ms.date: 4/26/2023
ms.keywords: IVMRSurface interface [DirectShow],UnlockSurface method, IVMRSurface.UnlockSurface, IVMRSurface::UnlockSurface, IVMRSurfaceUnlockSurface, UnlockSurface, UnlockSurface method [DirectShow], UnlockSurface method [DirectShow],IVMRSurface interface, dshow.ivmrsurface_unlocksurface, strmif/IVMRSurface::UnlockSurface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IVMRSurface::UnlockSurface
 - strmif/IVMRSurface::UnlockSurface
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
 - IVMRSurface.UnlockSurface
---

# IVMRSurface::UnlockSurface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>UnlockSurface</code> method unlocks the attached DirectDraw surface.



## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
No DirectDraw surface is attached to this sample.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrsurface">IVMRSurface Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
