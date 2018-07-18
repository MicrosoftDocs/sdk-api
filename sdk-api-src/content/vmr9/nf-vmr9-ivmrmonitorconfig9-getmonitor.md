---
UID: NF:vmr9.IVMRMonitorConfig9.GetMonitor
title: IVMRMonitorConfig9::GetMonitor
author: windows-sdk-content
description: The GetMonitor method retrieves the monitor that this instance of the VMR is using for video playback.
old-location: dshow\ivmrmonitorconfig9_getmonitor.htm
old-project: DirectShow
ms.assetid: 8b3e19d2-23de-42ae-9e5b-d53e24bb764a
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GetMonitor, GetMonitor method [DirectShow], GetMonitor method [DirectShow],IVMRMonitorConfig9 interface, IVMRMonitorConfig9 interface [DirectShow],GetMonitor method, IVMRMonitorConfig9.GetMonitor, IVMRMonitorConfig9::GetMonitor, IVMRMonitorConfig9GetMonitor, dshow.ivmrmonitorconfig9_getmonitor, vmr9/IVMRMonitorConfig9::GetMonitor
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VMR9DeinterlaceTech
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRMonitorConfig9.GetMonitor
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRMonitorConfig9::GetMonitor


## -description



The <code>GetMonitor</code> method retrieves the monitor that this instance of the VMR is using for video playback.




## -parameters




### -param puDev [out]

Pointer that receives an index that identifies the monitor currently in use.


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



Use this method to determine the Direct3D object that will be used when connecting the mixer filter to an upstream decoder filter.

Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://msdn.microsoft.com/27a3a598-d8de-48b2-8b8c-6b5497db4c6c">IVMRMonitorConfig9 Interface</a>



<a href="https://msdn.microsoft.com/21b0db95-3b70-4d9a-b533-393e89e106ae">IVMRMonitorConfig9::SetMonitor</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

