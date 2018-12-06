---
UID: NF:strmif.IVMRMonitorConfig.GetDefaultMonitor
title: IVMRMonitorConfig::GetDefaultMonitor
author: windows-sdk-content
description: The GetDefaultMonitor method retrieves the default monitor that all future instances of the VMR will use for video playback.
old-location: dshow\ivmrmonitorconfig_getdefaultmonitor.htm
tech.root: DirectShow
ms.assetid: 354b7f6e-35f8-4824-b5b5-24a37166462b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDefaultMonitor, GetDefaultMonitor method [DirectShow], GetDefaultMonitor method [DirectShow],IVMRMonitorConfig interface, IVMRMonitorConfig interface [DirectShow],GetDefaultMonitor method, IVMRMonitorConfig.GetDefaultMonitor, IVMRMonitorConfig::GetDefaultMonitor, IVMRMonitorConfigGetDefaultMonitor, dshow.ivmrmonitorconfig_getdefaultmonitor, strmif/IVMRMonitorConfig::GetDefaultMonitor
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
 - IVMRMonitorConfig.GetDefaultMonitor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRMonitorConfig::GetDefaultMonitor


## -description



The <code>GetDefaultMonitor</code> method retrieves the default monitor that all future instances of the VMR will use for video playback.




## -parameters




### -param pGUID [out]

Pointer to a <a href="https://msdn.microsoft.com/e05d986a-c044-47c9-8430-7190ad29c7ec">VMRGUID</a> structure that identifies the default monitor on the system.


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
 




## -remarks



Use this method on a multi-monitor system to determine which is the default DirectDraw device the VMR will use when connecting to an upstream filter.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/02b4016b-a65b-41ac-b5c6-e5f6825f179c">IVMRMonitorConfig Interface</a>



<a href="https://msdn.microsoft.com/85757536-ab7d-4b68-9e04-cf04fc4ebd5e">IVMRMonitorConfig::SetDefaultMonitor</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

