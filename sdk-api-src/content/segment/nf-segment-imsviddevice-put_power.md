---
UID: NF:segment.IMSVidDevice.put_Power
title: IMSVidDevice::put_Power
author: windows-sdk-content
description: The put_Power method turns the device on or off.
old-location: mstv\imsviddevice_put_power.htm
old-project: mstv
ms.assetid: 6a0122a8-6015-4255-a7d6-ab72b4025bd6
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMSVidDevice interface [Microsoft TV Technologies],put_Power method, IMSVidDevice.put_Power, IMSVidDevice::put_Power, IMSVidDeviceput_Power, mstv.imsviddevice_put_power, put_Power, put_Power method [Microsoft TV Technologies], put_Power method [Microsoft TV Technologies],IMSVidDevice interface, segment/IMSVidDevice::put_Power
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SourceSizeList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidDevice.put_Power
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidDevice::put_Power


## -description


The <b>put_Power</b> method turns the device on or off.


## -parameters




### -param Power [in]

Specifies whether to turn the power on or off. Use one of the following values.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>Turn the device on.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>Turn the device off.</td>
</tr>
</table>
 


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
</table>
 




## -remarks



Not all device types implement this method.




## -see-also




<a href="https://msdn.microsoft.com/5ec85d18-2fed-4fd0-ab94-72d1d4f3f7ef">IMSVidDevice Interface</a>



<a href="https://msdn.microsoft.com/3be4247b-43d4-4a32-8643-7eb2637aee6f">IMSVidDevice::get_Power</a>
 

 

