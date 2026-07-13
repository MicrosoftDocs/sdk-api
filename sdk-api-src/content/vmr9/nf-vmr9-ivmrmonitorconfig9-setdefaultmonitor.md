---
UID: NF:vmr9.IVMRMonitorConfig9.SetDefaultMonitor
title: IVMRMonitorConfig9::SetDefaultMonitor (vmr9.h)
description: The SetDefaultMonitor method specifies the default monitor that all future instances of the VMR should use for video playback.
helpviewer_keywords: ["IVMRMonitorConfig9 interface [DirectShow]","SetDefaultMonitor method","IVMRMonitorConfig9.SetDefaultMonitor","IVMRMonitorConfig9::SetDefaultMonitor","IVMRMonitorConfig9SetDefaultMonitor","SetDefaultMonitor","SetDefaultMonitor method [DirectShow]","SetDefaultMonitor method [DirectShow]","IVMRMonitorConfig9 interface","dshow.ivmrmonitorconfig9_setdefaultmonitor","vmr9/IVMRMonitorConfig9::SetDefaultMonitor"]
old-location: dshow\ivmrmonitorconfig9_setdefaultmonitor.htm
tech.root: dshow
ms.assetid: 4e02e0b6-8c0e-4c32-9059-91b1b8be165f
ms.date: 4/26/2023
ms.keywords: IVMRMonitorConfig9 interface [DirectShow],SetDefaultMonitor method, IVMRMonitorConfig9.SetDefaultMonitor, IVMRMonitorConfig9::SetDefaultMonitor, IVMRMonitorConfig9SetDefaultMonitor, SetDefaultMonitor, SetDefaultMonitor method [DirectShow], SetDefaultMonitor method [DirectShow],IVMRMonitorConfig9 interface, dshow.ivmrmonitorconfig9_setdefaultmonitor, vmr9/IVMRMonitorConfig9::SetDefaultMonitor
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
 - IVMRMonitorConfig9::SetDefaultMonitor
 - vmr9/IVMRMonitorConfig9::SetDefaultMonitor
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
 - IVMRMonitorConfig9.SetDefaultMonitor
---

# IVMRMonitorConfig9::SetDefaultMonitor


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetDefaultMonitor</code> method specifies the default monitor that all future instances of the VMR should use for video playback.

## -parameters

### -param uDev [in]

Index that specifies the default monitor.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Could not set the specified monitor as the default.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument; <i>uDev</i> does not correspond to a valid monitor.

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

Use this method on a multi-monitor system to specify to the VMR the default Direct3D device to use when connecting to an upstream filter. The default Direct3D device can be overridden for a particular connection by the <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrmonitorconfig9-setmonitor">SetMonitor</a> method.

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrmonitorconfig9">IVMRMonitorConfig9 Interface</a>



<a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrmonitorconfig9-getdefaultmonitor">IVMRMonitorConfig9::GetDefaultMonitor</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>