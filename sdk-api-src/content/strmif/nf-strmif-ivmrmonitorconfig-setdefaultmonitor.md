---
UID: NF:strmif.IVMRMonitorConfig.SetDefaultMonitor
title: IVMRMonitorConfig::SetDefaultMonitor
author: windows-driver-content
description: The SetDefaultMonitor method specifies the default monitor that all future instances of the VMR should use for video playback.
old-location: dshow\ivmrmonitorconfig_setdefaultmonitor.htm
old-project: DirectShow
ms.assetid: 85757536-ab7d-4b68-9e04-cf04fc4ebd5e
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IVMRMonitorConfig interface [DirectShow],SetDefaultMonitor method, IVMRMonitorConfig.SetDefaultMonitor, IVMRMonitorConfig::SetDefaultMonitor, IVMRMonitorConfigSetDefaultMonitor, SetDefaultMonitor, SetDefaultMonitor method [DirectShow], SetDefaultMonitor method [DirectShow],IVMRMonitorConfig interface, dshow.ivmrmonitorconfig_setdefaultmonitor, strmif/IVMRMonitorConfig::SetDefaultMonitor
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IVMRMonitorConfig.SetDefaultMonitor
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRMonitorConfig::SetDefaultMonitor


## -description



The <code>SetDefaultMonitor</code> method specifies the default monitor that all future instances of the VMR should use for video playback.




## -parameters




### -param pGUID [in]

Pointer to a <a href="https://msdn.microsoft.com/e05d986a-c044-47c9-8430-7190ad29c7ec">VMRGUID</a> structure that identifies the monitor.


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



Use this method on a multi-monitor system to specify to the VMR the default DirectDraw device to use when connecting to an upstream filter. The default DirectDraw device can be overriden for a particular connection by the <a href="https://msdn.microsoft.com/d443592e-23d8-425c-9f88-f4f786fb19c6">SetMonitor</a> method.

The <b>pGUID</b> member of the VMRGUID structure must be either <b>NULL</b>, indicating the default DirectDraw device, or equal to the address of the <b>GUID</b> member of the <b>VMRGUID</b> structure. Otherwise, the method returns E_INVALIDARG.

If the specified GUID does not correspond to any monitor, the method return E_INVALIDARG.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/02b4016b-a65b-41ac-b5c6-e5f6825f179c">IVMRMonitorConfig Interface</a>



<a href="https://msdn.microsoft.com/354b7f6e-35f8-4824-b5b5-24a37166462b">IVMRMonitorConfig::GetDefaultMonitor</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

