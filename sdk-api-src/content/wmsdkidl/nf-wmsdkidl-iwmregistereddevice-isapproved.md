---
UID: NF:wmsdkidl.IWMRegisteredDevice.IsApproved
title: IWMRegisteredDevice::IsApproved
author: windows-sdk-content
description: The IsApproved method retrieves the approval status of the device. Approved devices are able to receive and play media data.
old-location: wmformat\iwmregistereddevice_isapproved.htm
tech.root: wmformat
ms.assetid: ab90468e-743f-4367-a49b-d494bf9be28f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMRegisteredDevice interface [windows Media Format],IsApproved method, IWMRegisteredDevice.IsApproved, IWMRegisteredDevice::IsApproved, IWMRegisteredDeviceIsApproved, IsApproved, IsApproved method [windows Media Format], IsApproved method [windows Media Format],IWMRegisteredDevice interface, wmformat.iwmregistereddevice_isapproved, wmsdkidl/IWMRegisteredDevice::IsApproved
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
 - IWMRegisteredDevice.IsApproved
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMRegisteredDevice::IsApproved


## -description



The <b>IsApproved</b> method retrieves the approval status of the device. Approved devices are able to receive and play media data.




## -parameters




### -param pfApproved [out]

Address of a variable that receives the device approval status. <b>TRUE</b> indicates approval.


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

You can find out whether the device is open by calling <a href="https://msdn.microsoft.com/en-us/library/Dd743694(v=VS.85).aspx">IsOpened</a>. To open the device call <a href="https://msdn.microsoft.com/en-us/library/Dd743697(v=VS.85).aspx">Open</a>.

The device is valid only if proximity detection has been performed on it within the past 48 hours. You can check the validity of the device by calling <a href="https://msdn.microsoft.com/en-us/library/Dd743695(v=VS.85).aspx">IsValid</a>. For more information, see the <a href="https://msdn.microsoft.com/en-us/library/Dd757423(v=VS.85).aspx">IWMProximityDetection</a> interface.

Use this method to discover whether the device is approved. To approve the device, call the <a href="https://msdn.microsoft.com/en-us/library/Dd743624(v=VS.85).aspx">Approve</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743621(v=VS.85).aspx">IWMRegisteredDevice Interface</a>
 

 

