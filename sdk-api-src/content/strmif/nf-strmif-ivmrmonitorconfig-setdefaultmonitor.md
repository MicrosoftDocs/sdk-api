---
UID: NF:strmif.IVMRMonitorConfig.SetDefaultMonitor
title: IVMRMonitorConfig::SetDefaultMonitor (strmif.h)
description: The SetDefaultMonitor method specifies the default monitor that all future instances of the VMR should use for video playback.
helpviewer_keywords: ["IVMRMonitorConfig interface [DirectShow]","SetDefaultMonitor method","IVMRMonitorConfig.SetDefaultMonitor","IVMRMonitorConfig::SetDefaultMonitor","IVMRMonitorConfigSetDefaultMonitor","SetDefaultMonitor","SetDefaultMonitor method [DirectShow]","SetDefaultMonitor method [DirectShow]","IVMRMonitorConfig interface","dshow.ivmrmonitorconfig_setdefaultmonitor","strmif/IVMRMonitorConfig::SetDefaultMonitor"]
old-location: dshow\ivmrmonitorconfig_setdefaultmonitor.htm
tech.root: dshow
ms.assetid: 85757536-ab7d-4b68-9e04-cf04fc4ebd5e
ms.date: 4/26/2023
ms.keywords: IVMRMonitorConfig interface [DirectShow],SetDefaultMonitor method, IVMRMonitorConfig.SetDefaultMonitor, IVMRMonitorConfig::SetDefaultMonitor, IVMRMonitorConfigSetDefaultMonitor, SetDefaultMonitor, SetDefaultMonitor method [DirectShow], SetDefaultMonitor method [DirectShow],IVMRMonitorConfig interface, dshow.ivmrmonitorconfig_setdefaultmonitor, strmif/IVMRMonitorConfig::SetDefaultMonitor
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
 - IVMRMonitorConfig::SetDefaultMonitor
 - strmif/IVMRMonitorConfig::SetDefaultMonitor
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
 - IVMRMonitorConfig.SetDefaultMonitor
---

# IVMRMonitorConfig::SetDefaultMonitor


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetDefaultMonitor</code> method specifies the default monitor that all future instances of the VMR should use for video playback.

## -parameters

### -param pGUID [in]

Pointer to a [VMRGUID](/windows/desktop/api/strmif/ns-strmif-vmrguid) structure that identifies the monitor.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

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
Invalid argument. The specified monitor does not exist, or the pGUID parameter was not formatted correctly.

</td>
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
Success.

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

Use this method on a multi-monitor system to specify to the VMR the default DirectDraw device to use when connecting to an upstream filter. The default DirectDraw device can be overridden for a particular connection by the <a href="/windows/desktop/api/strmif/nf-strmif-ivmrmonitorconfig-setmonitor">SetMonitor</a> method.

The <b>pGUID</b> member of the VMRGUID structure must be either <b>NULL</b>, indicating the default DirectDraw device, or equal to the address of the <b>GUID</b> member of the <b>VMRGUID</b> structure. Otherwise, the method returns E_INVALIDARG.

If the specified GUID does not correspond to any monitor, the method return E_INVALIDARG.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrmonitorconfig">IVMRMonitorConfig Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrmonitorconfig-getdefaultmonitor">IVMRMonitorConfig::GetDefaultMonitor</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>