---
UID: NF:vmr9.IVMRMonitorConfig9.SetDefaultMonitor
title: IVMRMonitorConfig9::SetDefaultMonitor
author: windows-sdk-content
description: The SetDefaultMonitor method specifies the default monitor that all future instances of the VMR should use for video playback.
old-location: dshow\ivmrmonitorconfig9_setdefaultmonitor.htm
tech.root: DirectShow
ms.assetid: 4e02e0b6-8c0e-4c32-9059-91b1b8be165f
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IVMRMonitorConfig9 interface [DirectShow],SetDefaultMonitor method, IVMRMonitorConfig9.SetDefaultMonitor, IVMRMonitorConfig9::SetDefaultMonitor, IVMRMonitorConfig9SetDefaultMonitor, SetDefaultMonitor, SetDefaultMonitor method [DirectShow], SetDefaultMonitor method [DirectShow],IVMRMonitorConfig9 interface, dshow.ivmrmonitorconfig9_setdefaultmonitor, vmr9/IVMRMonitorConfig9::SetDefaultMonitor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- vmr9.h
: 
- IVMRMonitorConfig9.SetDefaultMonitor
: 
---

# IVMRMonitorConfig9::SetDefaultMonitor


## -description



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



Use this method on a multi-monitor system to specify to the VMR the default Direct3D device to use when connecting to an upstream filter. The default Direct3D device can be overridden for a particular connection by the <a href="https://msdn.microsoft.com/21b0db95-3b70-4d9a-b533-393e89e106ae">SetMonitor</a> method.

Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://msdn.microsoft.com/27a3a598-d8de-48b2-8b8c-6b5497db4c6c">IVMRMonitorConfig9 Interface</a>



<a href="https://msdn.microsoft.com/a5d5bf77-5261-42eb-b79b-d72dfb2d9f21">IVMRMonitorConfig9::GetDefaultMonitor</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

