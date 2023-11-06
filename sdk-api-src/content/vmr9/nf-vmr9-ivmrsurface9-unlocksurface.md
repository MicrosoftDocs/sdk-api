---
UID: NF:vmr9.IVMRSurface9.UnlockSurface
title: IVMRSurface9::UnlockSurface (vmr9.h)
description: The UnlockSurface method unlocks the attached Direct3D surface.
helpviewer_keywords: ["IVMRSurface9 interface [DirectShow]","UnlockSurface method","IVMRSurface9.UnlockSurface","IVMRSurface9::UnlockSurface","IVMRSurface9UnlockSurface","UnlockSurface","UnlockSurface method [DirectShow]","UnlockSurface method [DirectShow]","IVMRSurface9 interface","dshow.ivmrsurface9_unlocksurface","vmr9/IVMRSurface9::UnlockSurface"]
old-location: dshow\ivmrsurface9_unlocksurface.htm
tech.root: dshow
ms.assetid: 2785b1b7-62ed-420d-ab98-264e1b03b578
ms.date: 4/26/2023
ms.keywords: IVMRSurface9 interface [DirectShow],UnlockSurface method, IVMRSurface9.UnlockSurface, IVMRSurface9::UnlockSurface, IVMRSurface9UnlockSurface, UnlockSurface, UnlockSurface method [DirectShow], UnlockSurface method [DirectShow],IVMRSurface9 interface, dshow.ivmrsurface9_unlocksurface, vmr9/IVMRSurface9::UnlockSurface
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - IVMRSurface9::UnlockSurface
 - vmr9/IVMRSurface9::UnlockSurface
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
 - IVMRSurface9.UnlockSurface
---

# IVMRSurface9::UnlockSurface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>UnlockSurface</code> method unlocks the attached Direct3D surface.



## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
No Direct3D surface is attached to this sample.

</td>
</tr>
</table>

## -remarks

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/windows/desktop/api/vmr9/nn-vmr9-ivmrsurface9">IVMRSurface9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
