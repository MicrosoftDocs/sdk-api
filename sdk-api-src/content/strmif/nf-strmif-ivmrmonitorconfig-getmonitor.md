---
UID: NF:strmif.IVMRMonitorConfig.GetMonitor
title: IVMRMonitorConfig::GetMonitor (strmif.h)
description: The GetMonitor method retrieves the monitor that this instance of the VMR is using for video playback.
helpviewer_keywords: ["GetMonitor","GetMonitor method [DirectShow]","GetMonitor method [DirectShow]","IVMRMonitorConfig interface","IVMRMonitorConfig interface [DirectShow]","GetMonitor method","IVMRMonitorConfig.GetMonitor","IVMRMonitorConfig::GetMonitor","IVMRMonitorConfigGetMonitor","dshow.ivmrmonitorconfig_getmonitor","strmif/IVMRMonitorConfig::GetMonitor"]
old-location: dshow\ivmrmonitorconfig_getmonitor.htm
tech.root: dshow
ms.assetid: 8d71f1d1-4f8b-4ff8-9a4f-d25050821622
ms.date: 12/05/2018
ms.keywords: GetMonitor, GetMonitor method [DirectShow], GetMonitor method [DirectShow],IVMRMonitorConfig interface, IVMRMonitorConfig interface [DirectShow],GetMonitor method, IVMRMonitorConfig.GetMonitor, IVMRMonitorConfig::GetMonitor, IVMRMonitorConfigGetMonitor, dshow.ivmrmonitorconfig_getmonitor, strmif/IVMRMonitorConfig::GetMonitor
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
 - IVMRMonitorConfig::GetMonitor
 - strmif/IVMRMonitorConfig::GetMonitor
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
 - IVMRMonitorConfig.GetMonitor
---

# IVMRMonitorConfig::GetMonitor


## -description

The <code>GetMonitor</code> method retrieves the monitor that this instance of the VMR is using for video playback.

## -parameters

### -param pGUID [out]

Pointer to a [VMRGUID](/windows/desktop/api/strmif/ns-strmif-vmrguid) structure allocated by the caller. The method fills this structure with a GUID that identifies the monitor.

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

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrmonitorconfig">IVMRMonitorConfig Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrmonitorconfig-setmonitor">IVMRMonitorConfig::SetMonitor</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>