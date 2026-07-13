---
UID: NF:vmr9.IVMRSurfaceAllocator9.TerminateDevice
title: IVMRSurfaceAllocator9::TerminateDevice (vmr9.h)
description: The TerminateDevice method releases the Direct3D device.
helpviewer_keywords: ["IVMRSurfaceAllocator9 interface [DirectShow]","TerminateDevice method","IVMRSurfaceAllocator9.TerminateDevice","IVMRSurfaceAllocator9::TerminateDevice","IVMRSurfaceAllocator9TerminateDevice","TerminateDevice","TerminateDevice method [DirectShow]","TerminateDevice method [DirectShow]","IVMRSurfaceAllocator9 interface","dshow.ivmrsurfaceallocator9_terminatedevice","vmr9/IVMRSurfaceAllocator9::TerminateDevice"]
old-location: dshow\ivmrsurfaceallocator9_terminatedevice.htm
tech.root: dshow
ms.assetid: 5006265d-6f2b-433b-b3ce-a7074d6eb159
ms.date: 4/26/2023
ms.keywords: IVMRSurfaceAllocator9 interface [DirectShow],TerminateDevice method, IVMRSurfaceAllocator9.TerminateDevice, IVMRSurfaceAllocator9::TerminateDevice, IVMRSurfaceAllocator9TerminateDevice, TerminateDevice, TerminateDevice method [DirectShow], TerminateDevice method [DirectShow],IVMRSurfaceAllocator9 interface, dshow.ivmrsurfaceallocator9_terminatedevice, vmr9/IVMRSurfaceAllocator9::TerminateDevice
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
 - IVMRSurfaceAllocator9::TerminateDevice
 - vmr9/IVMRSurfaceAllocator9::TerminateDevice
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
 - IVMRSurfaceAllocator9.TerminateDevice
---

# IVMRSurfaceAllocator9::TerminateDevice


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>TerminateDevice</b> method releases the Direct3D device.

## -parameters

### -param dwID [in]

Application-defined identifier. This value is the same value that the application passed to the <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-advisesurfaceallocator">IVMRSurfaceAllocatorNotify9::AdviseSurfaceAllocator</a> method in the <i>dwUserID</i> parameter.

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

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrsurfaceallocator9">IVMRSurfaceAllocator9 Interface</a>



<a href="/windows/desktop/DirectShow/supplying-a-custom-allocator-presenter-for-vmr-9">Supplying a Custom Allocator-Presenter for VMR-9</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>