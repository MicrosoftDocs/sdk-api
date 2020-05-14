---
UID: NF:strmif.IVMRMonitorConfig.SetMonitor
title: IVMRMonitorConfig::SetMonitor (strmif.h)
description: On a multi-monitor system, the SetMonitor method specifies the monitor that this instance of the VMR should use for video playback.helpviewer_keywords: ["IVMRMonitorConfig interface [DirectShow]","SetMonitor method","IVMRMonitorConfig.SetMonitor","IVMRMonitorConfig::SetMonitor","IVMRMonitorConfigSetMonitor","SetMonitor","SetMonitor method [DirectShow]","SetMonitor method [DirectShow]","IVMRMonitorConfig interface","dshow.ivmrmonitorconfig_setmonitor","strmif/IVMRMonitorConfig::SetMonitor"]
old-location: dshow\ivmrmonitorconfig_setmonitor.htm
tech.root: DirectShow
ms.assetid: d443592e-23d8-425c-9f88-f4f786fb19c6
ms.date: 12/05/2018
ms.keywords: IVMRMonitorConfig interface [DirectShow],SetMonitor method, IVMRMonitorConfig.SetMonitor, IVMRMonitorConfig::SetMonitor, IVMRMonitorConfigSetMonitor, SetMonitor, SetMonitor method [DirectShow], SetMonitor method [DirectShow],IVMRMonitorConfig interface, dshow.ivmrmonitorconfig_setmonitor, strmif/IVMRMonitorConfig::SetMonitor
f1_keywords:
- strmif/IVMRMonitorConfig.SetMonitor
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IVMRMonitorConfig.SetMonitor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRMonitorConfig::SetMonitor


## -description



On a multi-monitor system, the <code>SetMonitor</code> method specifies the monitor that this instance of the VMR should use for video playback.




## -parameters




### -param pGUID [in]

Pointer to a [VMRGUID](https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-vmrguid) structure that identifies the monitor.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

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



Use this method on a multi-monitor system to specify to the VMR which DirectDraw driver should be used when connecting to an upstream decoder filter.

The <b>pGUID</b> member of the VMRGUID structure must be either <b>NULL</b>, indicating the default DirectDraw device, or equal to the address of the <b>GUID</b> member of the <b>VMRGUID</b> structure. Otherwise, the method returns E_INVALIDARG.

If the specified GUID does not correspond to any monitor, the method return E_INVALIDARG.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrmonitorconfig">IVMRMonitorConfig Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrmonitorconfig-getmonitor">IVMRMonitorConfig::GetMonitor</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

