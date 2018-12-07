---
UID: NF:strmif.IVMRMonitorConfig.GetMonitor
title: IVMRMonitorConfig::GetMonitor
author: windows-sdk-content
description: The GetMonitor method retrieves the monitor that this instance of the VMR is using for video playback.
old-location: dshow\ivmrmonitorconfig_getmonitor.htm
tech.root: DirectShow
ms.assetid: 8d71f1d1-4f8b-4ff8-9a4f-d25050821622
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetMonitor, GetMonitor method [DirectShow], GetMonitor method [DirectShow],IVMRMonitorConfig interface, IVMRMonitorConfig interface [DirectShow],GetMonitor method, IVMRMonitorConfig.GetMonitor, IVMRMonitorConfig::GetMonitor, IVMRMonitorConfigGetMonitor, dshow.ivmrmonitorconfig_getmonitor, strmif/IVMRMonitorConfig::GetMonitor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IVMRMonitorConfig.GetMonitor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRMonitorConfig::GetMonitor


## -description



The <code>GetMonitor</code> method retrieves the monitor that this instance of the VMR is using for video playback.




## -parameters




### -param pGUID [out]

Pointer to a <a href="https://msdn.microsoft.com/e05d986a-c044-47c9-8430-7190ad29c7ec">VMRGUID</a> structure allocated by the caller. The method fills this structure with a GUID that identifies the monitor.


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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/02b4016b-a65b-41ac-b5c6-e5f6825f179c">IVMRMonitorConfig Interface</a>



<a href="https://msdn.microsoft.com/d443592e-23d8-425c-9f88-f4f786fb19c6">IVMRMonitorConfig::SetMonitor</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

