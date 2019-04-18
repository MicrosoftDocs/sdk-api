---
UID: NF:strmif.IAMExtDevice.put_DevicePower
title: IAMExtDevice::put_DevicePower (strmif.h)
author: windows-sdk-content
description: The put_DevicePower method assigns the external device's power mode to either on, off, or standby.
old-location: dshow\iamextdevice_put_devicepower.htm
tech.root: DirectShow
ms.assetid: 9cb0c200-aaf4-44fb-b217-6a44a36089b5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMExtDevice interface [DirectShow],put_DevicePower method, IAMExtDevice.put_DevicePower, IAMExtDevice::put_DevicePower, IAMExtDeviceput_DevicePower, dshow.iamextdevice_put_devicepower, put_DevicePower, put_DevicePower method [DirectShow], put_DevicePower method [DirectShow],IAMExtDevice interface, strmif/IAMExtDevice::put_DevicePower
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IAMExtDevice.put_DevicePower
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMExtDevice::put_DevicePower


## -description



The <code>put_DevicePower</code> method assigns the external device's power mode to either on, off, or standby.




## -parameters




### -param PowerMode [in]

Specifies the device's power mode. Use one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_POWER_OFF</td>
<td>Off</td>
</tr>
<tr>
<td>ED_POWER_ON</td>
<td>On</td>
</tr>
<tr>
<td>ED_POWER_STANDBY</td>
<td>Standby</td>
</tr>
</table>
 


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0423e888-39d1-45cb-9bcf-722240a31fbd">IAMExtDevice Interface</a>



<a href="https://msdn.microsoft.com/7f25aac8-13ad-4ea2-96df-351da4729666">IAMExtDevice::get_DevicePower</a>
 

 

