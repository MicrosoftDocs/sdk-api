---
UID: NF:vmr9.IVMRMonitorConfig9.GetAvailableMonitors
title: IVMRMonitorConfig9::GetAvailableMonitors (vmr9.h)
author: windows-sdk-content
description: The GetAvailableMonitors method retrieves information about the monitors currently available on the system.
old-location: dshow\ivmrmonitorconfig9_getavailablemonitors.htm
tech.root: DirectShow
ms.assetid: cebd40c2-ea41-4ed1-87d1-37f9d427c539
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetAvailableMonitors, GetAvailableMonitors method [DirectShow], GetAvailableMonitors method [DirectShow],IVMRMonitorConfig9 interface, IVMRMonitorConfig9 interface [DirectShow],GetAvailableMonitors method, IVMRMonitorConfig9.GetAvailableMonitors, IVMRMonitorConfig9::GetAvailableMonitors, IVMRMonitorConfig9GetAvailableMonitors, dshow.ivmrmonitorconfig9_getavailablemonitors, vmr9/IVMRMonitorConfig9::GetAvailableMonitors
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
 - IVMRMonitorConfig9.GetAvailableMonitors
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRMonitorConfig9::GetAvailableMonitors


## -description



The <code>GetAvailableMonitors</code> method retrieves information about the monitors currently available on the system.




## -parameters




### -param pInfo [out]

Pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/Dd407368(v=VS.85).aspx">VMR9MonitorInfo</a> structures that contain information about each monitor on the system.


### -param dwMaxInfoArraySize [in]

Specifies the maximum number of members in the array.


### -param pdwNumDevices [out]

If <i>pInfo</i> is <b>NULL</b>, this parameter receives the required array size. Otherwise, it receives the actual number of devices retrieved.


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
Invalid argument; <i>dwMaxInfoArraySize</i> must be greater than zero.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



Use this method to get a list of Direct Draw device identifiers and their associated monitor information that the mixer can use when connecting to an upstream decoder filter.

Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd390482(v=VS.85).aspx">IVMRMonitorConfig9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

