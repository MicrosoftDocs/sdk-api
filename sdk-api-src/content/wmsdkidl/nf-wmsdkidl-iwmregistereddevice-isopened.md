---
UID: NF:wmsdkidl.IWMRegisteredDevice.IsOpened
title: IWMRegisteredDevice::IsOpened
author: windows-sdk-content
description: The IsOpened method retrieves the open status of the device. An open device is ready to receive media data.
old-location: wmformat\iwmregistereddevice_isopened.htm
tech.root: wmformat
ms.assetid: 5a8a6b2a-6a04-4505-b4be-ec10e1e5effe
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMRegisteredDevice interface [windows Media Format],IsOpened method, IWMRegisteredDevice.IsOpened, IWMRegisteredDevice::IsOpened, IWMRegisteredDeviceIsOpened, IsOpened, IsOpened method [windows Media Format], IsOpened method [windows Media Format],IWMRegisteredDevice interface, wmformat.iwmregistereddevice_isopened, wmsdkidl/IWMRegisteredDevice::IsOpened
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
 - IWMRegisteredDevice.IsOpened
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMRegisteredDevice::IsOpened


## -description



The <b>IsOpened</b> method retrieves the open status of the device. An open device is ready to receive media data.




## -parameters




### -param pfOpened [out]

Address of a variable that receives the open status of the device. <b>TRUE</b> indicates that the device is open.


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

You can use this method to find out whether the device is open. To open the device call <a href="https://msdn.microsoft.com/en-us/library/Dd743697(v=VS.85).aspx">Open</a>.

The device is valid only if proximity detection has been performed on it within the past 48 hours. You can check the validity of the device by calling <a href="https://msdn.microsoft.com/en-us/library/Dd743695(v=VS.85).aspx">IsValid</a>. For more information, see the <a href="https://msdn.microsoft.com/en-us/library/Dd757423(v=VS.85).aspx">IWMProximityDetection</a> interface.

Call the <a href="https://msdn.microsoft.com/en-us/library/Dd743693(v=VS.85).aspx">IsApproved</a> method to determine whether the device is approved. To approve the device, call the <a href="https://msdn.microsoft.com/en-us/library/Dd743624(v=VS.85).aspx">Approve</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743621(v=VS.85).aspx">IWMRegisteredDevice Interface</a>
 

 

