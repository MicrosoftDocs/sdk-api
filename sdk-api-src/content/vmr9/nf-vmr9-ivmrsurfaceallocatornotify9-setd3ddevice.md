---
UID: NF:vmr9.IVMRSurfaceAllocatorNotify9.SetD3DDevice
title: IVMRSurfaceAllocatorNotify9::SetD3DDevice (vmr9.h)
description: The SetD3DDevice method sets the Direct3D device.
helpviewer_keywords: ["IVMRSurfaceAllocatorNotify9 interface [DirectShow]","SetD3DDevice method","IVMRSurfaceAllocatorNotify9.SetD3DDevice","IVMRSurfaceAllocatorNotify9::SetD3DDevice","IVMRSurfaceAllocatorNotify9SetD3DDevice","SetD3DDevice","SetD3DDevice method [DirectShow]","SetD3DDevice method [DirectShow]","IVMRSurfaceAllocatorNotify9 interface","dshow.ivmrsurfaceallocatornotify9_setd3ddevice","vmr9/IVMRSurfaceAllocatorNotify9::SetD3DDevice"]
old-location: dshow\ivmrsurfaceallocatornotify9_setd3ddevice.htm
tech.root: dshow
ms.assetid: f13fd7f4-03b3-4e10-9fe8-b81470b37253
ms.date: 4/26/2023
ms.keywords: IVMRSurfaceAllocatorNotify9 interface [DirectShow],SetD3DDevice method, IVMRSurfaceAllocatorNotify9.SetD3DDevice, IVMRSurfaceAllocatorNotify9::SetD3DDevice, IVMRSurfaceAllocatorNotify9SetD3DDevice, SetD3DDevice, SetD3DDevice method [DirectShow], SetD3DDevice method [DirectShow],IVMRSurfaceAllocatorNotify9 interface, dshow.ivmrsurfaceallocatornotify9_setd3ddevice, vmr9/IVMRSurfaceAllocatorNotify9::SetD3DDevice
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
 - IVMRSurfaceAllocatorNotify9::SetD3DDevice
 - vmr9/IVMRSurfaceAllocatorNotify9::SetD3DDevice
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
 - IVMRSurfaceAllocatorNotify9.SetD3DDevice
---

# IVMRSurfaceAllocatorNotify9::SetD3DDevice


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetD3DDevice</code> method sets the Direct3D device.

## -parameters

### -param lpD3DDevice [in]

Pointer to the <b>IDirect3DDevice9</b> interface of the device.

### -param hMonitor [in]

Handle to a monitor.

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
</table>

## -remarks

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrsurfaceallocatornotify9">IVMRSurfaceAllocatorNotify9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>