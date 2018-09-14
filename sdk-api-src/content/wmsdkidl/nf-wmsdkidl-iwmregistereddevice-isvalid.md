---
UID: NF:wmsdkidl.IWMRegisteredDevice.IsValid
title: IWMRegisteredDevice::IsValid
author: windows-sdk-content
description: The IsValid method retrieves the validation status of the device.
old-location: wmformat\iwmregistereddevice_isvalid.htm
tech.root: wmformat
ms.assetid: ce09e6ad-10c0-4cdd-8dee-4faacd958f2b
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWMRegisteredDevice interface [windows Media Format],IsValid method, IWMRegisteredDevice.IsValid, IWMRegisteredDevice::IsValid, IWMRegisteredDeviceIsValid, IsValid, IsValid method [windows Media Format], IsValid method [windows Media Format],IWMRegisteredDevice interface, wmformat.iwmregistereddevice_isvalid, wmsdkidl/IWMRegisteredDevice::IsValid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9.5 SDK
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
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMRegisteredDevice.IsValid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMRegisteredDevice::IsValid


## -description



The <b>IsValid</b> method retrieves the validation status of the device.




## -parameters




### -param pfValid [out]

Address of a variable that receives the validation status of the device. <b>TRUE</b> indicates that the device is valid. <b>FALSE</b> indicates that the device is not valid and needs to be revalidated before it can be used.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



To receive data, a device must be opened, validated, and approved.

You can find out whether the device is open by calling <a href="https://msdn.microsoft.com/5a8a6b2a-6a04-4505-b4be-ec10e1e5effe">IsOpened</a>. To open the device call <a href="https://msdn.microsoft.com/277f2724-5d82-4db7-96d9-af392b39fccf">Open</a>.

A device is validated by performing proximity detection. For more information, see the <a href="https://msdn.microsoft.com/0897ad8f-8e06-4de9-840e-1588e0e20c54">IWMProximityDetection</a> interface.

Call the <a href="https://msdn.microsoft.com/ab90468e-743f-4367-a49b-d494bf9be28f">IsApproved</a> method to determine whether the device is approved. To approve the device, call the <a href="https://msdn.microsoft.com/941714b8-c329-4768-9c48-86fa806550c3">Approve</a> method.




## -see-also




<a href="https://msdn.microsoft.com/6babdfbd-51d5-4973-9712-f79a95f5f367">IWMRegisteredDevice Interface</a>
 

 

