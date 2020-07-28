---
UID: NF:wmsdkidl.IWMRegisteredDevice.Approve
title: IWMRegisteredDevice::Approve (wmsdkidl.h)
description: The Approve method sets the approval state of the device for receiving media data.
helpviewer_keywords: ["Approve","Approve method [windows Media Format]","Approve method [windows Media Format]","IWMRegisteredDevice interface","IWMRegisteredDevice interface [windows Media Format]","Approve method","IWMRegisteredDevice.Approve","IWMRegisteredDevice::Approve","IWMRegisteredDeviceApprove","wmformat.iwmregistereddevice_approve","wmsdkidl/IWMRegisteredDevice::Approve"]
old-location: wmformat\iwmregistereddevice_approve.htm
tech.root: wmformat
ms.assetid: 941714b8-c329-4768-9c48-86fa806550c3
ms.date: 12/05/2018
ms.keywords: Approve, Approve method [windows Media Format], Approve method [windows Media Format],IWMRegisteredDevice interface, IWMRegisteredDevice interface [windows Media Format],Approve method, IWMRegisteredDevice.Approve, IWMRegisteredDevice::Approve, IWMRegisteredDeviceApprove, wmformat.iwmregistereddevice_approve, wmsdkidl/IWMRegisteredDevice::Approve
f1_keywords:
- wmsdkidl/IWMRegisteredDevice.Approve
dev_langs:
- c++
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
- IWMRegisteredDevice.Approve
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMRegisteredDevice::Approve


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

You can find out whether the device is open by calling <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isopened">IsOpened</a>. To open the device call <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open">Open</a>.

The device is valid only if proximity detection has been performed on it within the past 48 hours. You can check the validity of the device by calling <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid">IsValid</a>. For more information, see the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection">IWMProximityDetection</a> interface.

Call the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isapproved">IsApproved</a> method to determine whether the device is approved. Use <b>Approve</b> to approve or restrict the device.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice">IWMRegisteredDevice Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isapproved">IWMRegisteredDevice::IsApproved</a>
 

 

