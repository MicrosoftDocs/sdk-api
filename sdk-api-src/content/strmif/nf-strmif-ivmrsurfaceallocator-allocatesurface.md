---
UID: NF:strmif.IVMRSurfaceAllocator.AllocateSurface
title: IVMRSurfaceAllocator::AllocateSurface (strmif.h)
description: The AllocateSurface method allocates a DirectDraw surface.
helpviewer_keywords: ["AllocateSurface","AllocateSurface method [DirectShow]","AllocateSurface method [DirectShow]","IVMRSurfaceAllocator interface","IVMRSurfaceAllocator interface [DirectShow]","AllocateSurface method","IVMRSurfaceAllocator.AllocateSurface","IVMRSurfaceAllocator::AllocateSurface","IVMRSurfaceAllocatorAllocateSurface","dshow.ivmrsurfaceallocator_allocatesurface","strmif/IVMRSurfaceAllocator::AllocateSurface"]
old-location: dshow\ivmrsurfaceallocator_allocatesurface.htm
tech.root: dshow
ms.assetid: 6783df91-c92f-45d0-b299-16cdbc4bb630
ms.date: 4/26/2023
ms.keywords: AllocateSurface, AllocateSurface method [DirectShow], AllocateSurface method [DirectShow],IVMRSurfaceAllocator interface, IVMRSurfaceAllocator interface [DirectShow],AllocateSurface method, IVMRSurfaceAllocator.AllocateSurface, IVMRSurfaceAllocator::AllocateSurface, IVMRSurfaceAllocatorAllocateSurface, dshow.ivmrsurfaceallocator_allocatesurface, strmif/IVMRSurfaceAllocator::AllocateSurface
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
 - IVMRSurfaceAllocator::AllocateSurface
 - strmif/IVMRSurfaceAllocator::AllocateSurface
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
 - IVMRSurfaceAllocator.AllocateSurface
---

# IVMRSurfaceAllocator::AllocateSurface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>AllocateSurface</code> method allocates a DirectDraw surface.

## -parameters

### -param dwUserID [in]

An application-defined DWORD_PTR cookie that uniquely identifies this instance of the VMR for use in scenarios when one instance of the allocator-presenter is used with multiple VMR instances.

### -param lpAllocInfo [in]

Specifies the [VMRALLOCATIONINFO](/windows/desktop/api/strmif/ns-strmif-vmrallocationinfo) structure. See Remarks.

### -param lpdwActualBuffers [in]

[out] On input this parameter is used to request the number of buffers desired. On output it receives the actual number of buffers created.

### -param lplpSurface [out]

Address of a pointer that receives the Direct3D surface.

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
One of the pointers is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
In <i>dwFlags</i>, the AMAP_3D_TARGET was combined with AMAP_FORCE_SYSMEM or AMAP_ALLOW_SYSMEM.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
One or more members of the BITMAPINFOHEADER structure specified by <i>lpAllocInfo</i>-&gt;lpHdr is incorrect.

</td>
</tr>
</table>

## -remarks

Before calling <b>AllocateSurface</b> explicitly, a client application should call <a href="/windows/desktop/api/strmif/nf-strmif-ivmrsurfaceallocator-freesurface">IVMRSurfaceAllocator::FreeSurface</a> to be sure that the DirectDraw decoding surface front buffer is <b>NULL</b>. If it is not <b>NULL</b> at the time an application calls <b>AllocateSurface</b>, the debug version of quartz.dll will cause an assertion.

When implementing this method in a custom allocator-presenter, you must examine the value of <i>lpAllocInfo</i>-&gt;lpHdr-&gt;biBitCount. If biBitCount is zero, then you must set it to the pixel depth for the current display. If BiBitCount is left at zero, the surface allocation will fail and a new (default) VMR will be created.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrsurfaceallocator">IVMRSurfaceAllocator Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>