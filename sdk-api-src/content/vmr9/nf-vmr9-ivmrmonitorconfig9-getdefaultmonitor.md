---
UID: NF:vmr9.IVMRMonitorConfig9.GetDefaultMonitor
title: IVMRMonitorConfig9::GetDefaultMonitor (vmr9.h)
description: The GetDefaultMonitor method retrieves the default monitor that all future instances of the VMR will use for video playback.
helpviewer_keywords: ["GetDefaultMonitor","GetDefaultMonitor method [DirectShow]","GetDefaultMonitor method [DirectShow]","IVMRMonitorConfig9 interface","IVMRMonitorConfig9 interface [DirectShow]","GetDefaultMonitor method","IVMRMonitorConfig9.GetDefaultMonitor","IVMRMonitorConfig9::GetDefaultMonitor","IVMRMonitorConfig9GetDefaultMonitor","dshow.ivmrmonitorconfig9_getdefaultmonitor","vmr9/IVMRMonitorConfig9::GetDefaultMonitor"]
old-location: dshow\ivmrmonitorconfig9_getdefaultmonitor.htm
tech.root: dshow
ms.assetid: a5d5bf77-5261-42eb-b79b-d72dfb2d9f21
ms.date: 4/26/2023
ms.keywords: GetDefaultMonitor, GetDefaultMonitor method [DirectShow], GetDefaultMonitor method [DirectShow],IVMRMonitorConfig9 interface, IVMRMonitorConfig9 interface [DirectShow],GetDefaultMonitor method, IVMRMonitorConfig9.GetDefaultMonitor, IVMRMonitorConfig9::GetDefaultMonitor, IVMRMonitorConfig9GetDefaultMonitor, dshow.ivmrmonitorconfig9_getdefaultmonitor, vmr9/IVMRMonitorConfig9::GetDefaultMonitor
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
 - IVMRMonitorConfig9::GetDefaultMonitor
 - vmr9/IVMRMonitorConfig9::GetDefaultMonitor
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
 - IVMRMonitorConfig9.GetDefaultMonitor
---

# IVMRMonitorConfig9::GetDefaultMonitor


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetDefaultMonitor</code> method retrieves the default monitor that all future instances of the VMR will use for video playback.

## -parameters

### -param puDev [out]

Pointer that receives an index that identifies the default monitor on the system.

## -returns

The method returns an <b>HRESULT</b>. Possible values include the following.

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
<b>NULL</b> pointer argument.

</td>
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
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The allocator-presenter has not been loaded.

</td>
</tr>
</table>

## -remarks

Use this method on a multi-monitor system to determine which is the default Direct3D device the overlay mixer filter will use when connecting to an upstream filter.

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrmonitorconfig9">IVMRMonitorConfig9 Interface</a>



<a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrmonitorconfig9-setdefaultmonitor">IVMRMonitorConfig9::SetDefaultMonitor</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>