---
UID: NF:strmif.IVMRMonitorConfig.GetAvailableMonitors
title: IVMRMonitorConfig::GetAvailableMonitors method
author: windows-driver-content
description: The GetAvailableMonitors method retrieves information about the monitors currently available on the system.
old-location: dshow\ivmrmonitorconfig_getavailablemonitors.htm
old-project: DirectShow
ms.assetid: 8a44ca7d-a195-4fcf-b09c-01f8176e0aa2
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetAvailableMonitors method [DirectShow], GetAvailableMonitors method [DirectShow], IVMRMonitorConfig interface, GetAvailableMonitors,IVMRMonitorConfig.GetAvailableMonitors, IVMRMonitorConfig, IVMRMonitorConfig interface [DirectShow], GetAvailableMonitors method, IVMRMonitorConfig::GetAvailableMonitors, IVMRMonitorConfigGetAvailableMonitors, dshow.ivmrmonitorconfig_getavailablemonitors, strmif/IVMRMonitorConfig::GetAvailableMonitors
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
-	IVMRMonitorConfig.GetAvailableMonitors
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRMonitorConfig::GetAvailableMonitors method


## -description



The <code>GetAvailableMonitors</code> method retrieves information about the monitors currently available on the system.




## -parameters




### -param pInfo [out]

Pointer to an array of <a href="https://msdn.microsoft.com/87567836-c01e-4615-a8e7-9ca590b6f7c9">VMRMONITORINFO</a> structures that contain information about each monitor on the system.


### -param dwMaxInfoArraySize [in]

Specifies the maximum number of members in the array.


### -param pdwNumDevices [out]

Pointer to a variable that receives the number of devices retrieved.



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
Success.

</td>
</tr>
</table>
 




## -remarks



Use this method to get a list of DirectDraw device GUIDs and their associated monitor information that the VMR can use when connecting to an upstream decoder filter. To return the required array size in the <i>pdwNumDevices</i> parameter, specify <b>NULL</b> for <i>pInfo</i>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/02b4016b-a65b-41ac-b5c6-e5f6825f179c">IVMRMonitorConfig Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

