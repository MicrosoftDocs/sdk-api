---
UID: NF:strmif.IAMExtDevice.put_DevicePower
title: IAMExtDevice::put_DevicePower (strmif.h)
description: The put_DevicePower method assigns the external device's power mode to either on, off, or standby.
helpviewer_keywords: ["IAMExtDevice interface [DirectShow]","put_DevicePower method","IAMExtDevice.put_DevicePower","IAMExtDevice::put_DevicePower","IAMExtDeviceput_DevicePower","dshow.iamextdevice_put_devicepower","put_DevicePower","put_DevicePower method [DirectShow]","put_DevicePower method [DirectShow]","IAMExtDevice interface","strmif/IAMExtDevice::put_DevicePower"]
old-location: dshow\iamextdevice_put_devicepower.htm
tech.root: dshow
ms.assetid: 9cb0c200-aaf4-44fb-b217-6a44a36089b5
ms.date: 12/05/2018
ms.keywords: IAMExtDevice interface [DirectShow],put_DevicePower method, IAMExtDevice.put_DevicePower, IAMExtDevice::put_DevicePower, IAMExtDeviceput_DevicePower, dshow.iamextdevice_put_devicepower, put_DevicePower, put_DevicePower method [DirectShow], put_DevicePower method [DirectShow],IAMExtDevice interface, strmif/IAMExtDevice::put_DevicePower
f1_keywords:
- strmif/IAMExtDevice.put_DevicePower
dev_langs:
- c++
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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamextdevice">IAMExtDevice Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamextdevice-get_devicepower">IAMExtDevice::get_DevicePower</a>
 

 

