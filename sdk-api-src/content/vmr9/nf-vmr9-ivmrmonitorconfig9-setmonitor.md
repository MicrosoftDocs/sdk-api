---
UID: NF:vmr9.IVMRMonitorConfig9.SetMonitor
title: IVMRMonitorConfig9::SetMonitor
author: windows-sdk-content
description: On a multi-monitor system, the SetMonitor method specifies the monitor that the VMR should use when it creates the Direct3D device.
old-location: dshow\ivmrmonitorconfig9_setmonitor.htm
tech.root: DirectShow
ms.assetid: 21b0db95-3b70-4d9a-b533-393e89e106ae
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IVMRMonitorConfig9 interface [DirectShow],SetMonitor method, IVMRMonitorConfig9.SetMonitor, IVMRMonitorConfig9::SetMonitor, IVMRMonitorConfig9SetMonitor, SetMonitor, SetMonitor method [DirectShow], SetMonitor method [DirectShow],IVMRMonitorConfig9 interface, dshow.ivmrmonitorconfig9_setmonitor, vmr9/IVMRMonitorConfig9::SetMonitor
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
 - IVMRMonitorConfig9.SetMonitor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRMonitorConfig9::SetMonitor


## -description



On a multi-monitor system, the <code>SetMonitor</code> method specifies the monitor that the VMR should use when it creates the Direct3D device.




## -parameters




### -param uDev [in]

Index that specifies the monitor.


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
Cannot set the monitor after the VMR's input pins have been connected.

</td>
</tr>
</table>
 




## -remarks



Use this method on a multi-monitor system to specify to the VMR which Direct3D device should be used when connecting to an upstream decoder filter.

Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://msdn.microsoft.com/27a3a598-d8de-48b2-8b8c-6b5497db4c6c">IVMRMonitorConfig9 Interface</a>



<a href="https://msdn.microsoft.com/8b3e19d2-23de-42ae-9e5b-d53e24bb764a">IVMRMonitorConfig9::GetMonitor</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

