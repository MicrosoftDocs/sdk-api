---
UID: NF:vmr9.IVMRSurface9.GetSurface
title: IVMRSurface9::GetSurface (vmr9.h)
description: The GetSurface method retrieves the attached Direct3D surface.
helpviewer_keywords: ["GetSurface","GetSurface method [DirectShow]","GetSurface method [DirectShow]","IVMRSurface9 interface","IVMRSurface9 interface [DirectShow]","GetSurface method","IVMRSurface9.GetSurface","IVMRSurface9::GetSurface","IVMRSurface9GetSurface","dshow.ivmrsurface9_getsurface","vmr9/IVMRSurface9::GetSurface"]
old-location: dshow\ivmrsurface9_getsurface.htm
tech.root: dshow
ms.assetid: ce556b66-0a28-43a0-9dd2-a1c3b9aad5dc
ms.date: 4/26/2023
ms.keywords: GetSurface, GetSurface method [DirectShow], GetSurface method [DirectShow],IVMRSurface9 interface, IVMRSurface9 interface [DirectShow],GetSurface method, IVMRSurface9.GetSurface, IVMRSurface9::GetSurface, IVMRSurface9GetSurface, dshow.ivmrsurface9_getsurface, vmr9/IVMRSurface9::GetSurface
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
 - IVMRSurface9::GetSurface
 - vmr9/IVMRSurface9::GetSurface
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
 - IVMRSurface9.GetSurface
---

# IVMRSurface9::GetSurface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetSurface</code> method retrieves the attached Direct3D surface.

## -parameters

### -param lplpSurface [out]

Address of a variable that receives an <b>IDirect3DSurface9</b> interface pointer. The caller must release the interface.

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
<i>lplpSurface</i> is invalid.

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

The media sample object increments the reference count on the returned interface. The caller must call Release on the interface.

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/windows/desktop/api/vmr9/nn-vmr9-ivmrsurface9">IVMRSurface9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>