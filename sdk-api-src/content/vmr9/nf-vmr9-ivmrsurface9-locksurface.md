---
UID: NF:vmr9.IVMRSurface9.LockSurface
title: IVMRSurface9::LockSurface (vmr9.h)
description: The LockSurface method locks the attached Direct3D surface.
helpviewer_keywords: ["IVMRSurface9 interface [DirectShow]","LockSurface method","IVMRSurface9.LockSurface","IVMRSurface9::LockSurface","IVMRSurface9LockSurface","LockSurface","LockSurface method [DirectShow]","LockSurface method [DirectShow]","IVMRSurface9 interface","dshow.ivmrsurface9_locksurface","vmr9/IVMRSurface9::LockSurface"]
old-location: dshow\ivmrsurface9_locksurface.htm
tech.root: dshow
ms.assetid: fb185898-5d65-48ee-a7be-f4207199f5e9
ms.date: 4/26/2023
ms.keywords: IVMRSurface9 interface [DirectShow],LockSurface method, IVMRSurface9.LockSurface, IVMRSurface9::LockSurface, IVMRSurface9LockSurface, LockSurface, LockSurface method [DirectShow], LockSurface method [DirectShow],IVMRSurface9 interface, dshow.ivmrsurface9_locksurface, vmr9/IVMRSurface9::LockSurface
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
 - IVMRSurface9::LockSurface
 - vmr9/IVMRSurface9::LockSurface
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
 - IVMRSurface9.LockSurface
---

# IVMRSurface9::LockSurface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>LockSurface</code> method locks the attached Direct3D surface.

## -parameters

### -param lpSurface [out]

Address of a variable that receives a pointer to the locked bits.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer.

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