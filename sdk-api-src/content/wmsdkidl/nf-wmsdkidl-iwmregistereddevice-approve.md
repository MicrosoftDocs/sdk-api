---
UID: NF:wmsdkidl.IWMRegisteredDevice.Approve
title: IWMRegisteredDevice::Approve method
author: windows-driver-content
description: The Approve method sets the approval state of the device for receiving media data.
old-location: wmformat\iwmregistereddevice_approve.htm
old-project: wmformat
ms.assetid: 941714b8-c329-4768-9c48-86fa806550c3
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: Approve method [windows Media Format], Approve method [windows Media Format], IWMRegisteredDevice interface, Approve,IWMRegisteredDevice.Approve, IWMRegisteredDevice, IWMRegisteredDevice interface [windows Media Format], Approve method, IWMRegisteredDevice::Approve, IWMRegisteredDeviceApprove, wmformat.iwmregistereddevice_approve, wmsdkidl/IWMRegisteredDevice::Approve
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMRegisteredDevice.Approve
product: Windows
targetos: Windows
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMRegisteredDevice::Approve method


## -description



The <b>Approve</b> method sets the approval state of the device for receiving media data.




## -parameters




### -param fApprove [in]

Set to <b>TRUE</b> to approve the device for receiving media data; set to <b>FALSE</b> to indicate that the device is not approved.


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



Approval is a mechanism by which your application can approve a device for playback or prohibit it from being used for playback. A typical scenario would be to ask the user whether the device should be used, and to set approval accordingly.

To receive data, a device must be opened, validated, and approved.

You can find out whether the device is open by calling <a href="https://msdn.microsoft.com/5a8a6b2a-6a04-4505-b4be-ec10e1e5effe">IsOpened</a>. To open the device call <a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>.

The device is valid only if proximity detection has been performed on it within the past 48 hours. You can check the validity of the device by calling <a href="https://msdn.microsoft.com/ce09e6ad-10c0-4cdd-8dee-4faacd958f2b">IsValid</a>. For more information, see the <a href="https://msdn.microsoft.com/0897ad8f-8e06-4de9-840e-1588e0e20c54">IWMProximityDetection</a> interface.

Call the <a href="https://msdn.microsoft.com/ab90468e-743f-4367-a49b-d494bf9be28f">IsApproved</a> method to determine whether the device is approved. Use <b>Approve</b> to approve or restrict the device.




## -see-also




<a href="https://msdn.microsoft.com/6babdfbd-51d5-4973-9712-f79a95f5f367">IWMRegisteredDevice Interface</a>



<a href="https://msdn.microsoft.com/ab90468e-743f-4367-a49b-d494bf9be28f">IWMRegisteredDevice::IsApproved</a>
 

 

