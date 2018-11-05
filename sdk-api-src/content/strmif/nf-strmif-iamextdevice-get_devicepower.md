---
UID: NF:strmif.IAMExtDevice.get_DevicePower
title: IAMExtDevice::get_DevicePower
author: windows-sdk-content
description: The get_DevicePower method retrieves the external device's power mode.
old-location: dshow\iamextdevice_get_devicepower.htm
tech.root: DirectShow
ms.assetid: 7f25aac8-13ad-4ea2-96df-351da4729666
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IAMExtDevice interface [DirectShow],get_DevicePower method, IAMExtDevice.get_DevicePower, IAMExtDevice::get_DevicePower, IAMExtDeviceget_DevicePower, dshow.iamextdevice_get_devicepower, get_DevicePower, get_DevicePower method [DirectShow], get_DevicePower method [DirectShow],IAMExtDevice interface, strmif/IAMExtDevice::get_DevicePower
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IAMExtDevice.get_DevicePower
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMExtDevice::get_DevicePower


## -description



The <code>get_DevicePower</code> method retrieves the external device's power mode.




## -parameters




### -param pPowerMode [out]

Pointer to a <b>long</b> integer that receives one of the following values, indicating the device's power mode.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_POWER_OFF</td>
<td>Power is off.</td>
</tr>
<tr>
<td>ED_POWER_ON</td>
<td>Power if on.</td>
</tr>
<tr>
<td>ED_POWER_STANDBY</td>
<td>Device is in standby mode.</td>
</tr>
</table>
 


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -remarks



In Windows XP Service Pack 2 and later, the following additional power mode is defined.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>ED_POWER_DEVICE_DEPENDENT</td>
<td>Power is on with limited functions.</td>
</tr>
</table>
 

To use this constant, include the header file Xprtdefs.h.

<h3><a id="DV_and_MPEG_Camcorder_Implementation"></a><a id="dv_and_mpeg_camcorder_implementation"></a><a id="DV_AND_MPEG_CAMCORDER_IMPLEMENTATION"></a>DV and MPEG Camcorder Implementation</h3>
The <a href="https://msdn.microsoft.com/146ca753-fe41-49d3-8b1c-077e10a28192">MSDV</a> and UVC drivers return ED_POWER_ON when the camcorder is on. If the camcorder is off or in standby mode, the DV driver is not loaded, so this method is not available. If the camcorder is removed unexpectedly, the method can return ERROR_GEN_FAILURE.


<a href="https://msdn.microsoft.com/aa59f322-09b1-4b0a-be6f-d865c20f76e5">MSTape</a> supports both ED_POWER_OFF and ED_POWER_ON, but not ED_POWER_STANDBY.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0423e888-39d1-45cb-9bcf-722240a31fbd">IAMExtDevice Interface</a>



<a href="https://msdn.microsoft.com/9cb0c200-aaf4-44fb-b217-6a44a36089b5">IAMExtDevice::put_DevicePower</a>
 

 

