---
UID: NF:strmif.IVMRSurface.LockSurface
title: IVMRSurface::LockSurface (strmif.h)
description: The LockSurface method locks the attached DirectDraw surface.
helpviewer_keywords: ["IVMRSurface interface [DirectShow]","LockSurface method","IVMRSurface.LockSurface","IVMRSurface::LockSurface","IVMRSurfaceLockSurface","LockSurface","LockSurface method [DirectShow]","LockSurface method [DirectShow]","IVMRSurface interface","dshow.ivmrsurface_locksurface","strmif/IVMRSurface::LockSurface"]
old-location: dshow\ivmrsurface_locksurface.htm
tech.root: dshow
ms.assetid: 119a6983-3639-4047-b8b4-7a8b0cb5583d
ms.date: 4/26/2023
ms.keywords: IVMRSurface interface [DirectShow],LockSurface method, IVMRSurface.LockSurface, IVMRSurface::LockSurface, IVMRSurfaceLockSurface, LockSurface, LockSurface method [DirectShow], LockSurface method [DirectShow],IVMRSurface interface, dshow.ivmrsurface_locksurface, strmif/IVMRSurface::LockSurface
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
 - IVMRSurface::LockSurface
 - strmif/IVMRSurface::LockSurface
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
 - IVMRSurface.LockSurface
---

# IVMRSurface::LockSurface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>LockSurface</code> method locks the attached DirectDraw surface.

## -parameters

### -param lpSurface [out]

Address of a variable that receives a pointer to the locked bits.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>lpSurface</i> is invalid.

</td>
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