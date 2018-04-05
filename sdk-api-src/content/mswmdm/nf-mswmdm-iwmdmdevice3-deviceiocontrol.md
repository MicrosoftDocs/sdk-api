---
UID: NF:mswmdm.IWMDMDevice3.DeviceIoControl
title: IWMDMDevice3::DeviceIoControl method
author: windows-driver-content
description: The DeviceIoControl method sends a Device I/O Control (IOCTL) code to the device. This is a pass-through method; Windows Media Device Manager just forwards the call to the service provider after validating the parameters.
old-location: wmdm\iwmdmdevice3_deviceiocontrol.htm
old-project: WMDM
ms.assetid: 3ef6a95d-d4e2-4608-9a02-98b497e1fdbb
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: DeviceIoControl method [windows Media Device Manager], DeviceIoControl method [windows Media Device Manager], IWMDMDevice3 interface, DeviceIoControl,IWMDMDevice3.DeviceIoControl, IWMDMDevice3, IWMDMDevice3 interface [windows Media Device Manager], DeviceIoControl method, IWMDMDevice3::DeviceIoControl, IWMDMDevice3DeviceToControl, mswmdm/IWMDMDevice3::DeviceIoControl, wmdm.iwmdmdevice3_deviceiocontrol
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mssachlp.lib
-	mssachlp.dll
api_name:
-	IWMDMDevice3.DeviceIoControl
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IWMDMDevice3::DeviceIoControl method


## -description



The <b>DeviceIoControl</b> method sends a Device I/O Control (IOCTL) code to the device. This is a pass-through method; Windows Media Device Manager just forwards the call to the service provider after validating the parameters.




## -parameters




### -param dwIoControlCode [in]

Control code to send to the device. When calling this method on an MTP device, use the value IOCTL_MTP_CUSTOM_COMMAND defined in MtpExt.h included with the SDK.


### -param lpInBuffer [in]

Optional pointer to an input buffer supplied by the caller. It can be <b>NULL</b> if <i>nInBufferSize</i> is zero. When calling this method on an MTP device, you can pass in the <a href="https://msdn.microsoft.com/a7a6871b-3d53-4134-9877-398c532b489f">MTP_COMMAND_DATA_IN</a> structure.


### -param nInBufferSize [in]

Size of the input buffer, in bytes. When calling this method on an MTP device, you can use the macro <b>SIZEOF_REQUIRED_COMMAND_DATA_IN</b> to specify the size.


### -param lpOutBuffer [out]

Optional pointer to the output buffer supplied by the caller. It can be <b>NULL</b> if <i>pnOutBufferSize</i> points to a value of zero. When calling this method on an MTP device, you can pass in the <a href="https://msdn.microsoft.com/ddaf49c8-99df-4e21-a633-82e08691f088">MTP_COMMAND_DATA_OUT</a> structure.


### -param pnOutBufferSize [in, out]

Size of the output buffer, in bytes. When the call returns, it specifies the number of bytes actually returned. When calling this method on an MTP device, you can use the macro <b>SIZEOF_REQUIRED_COMMAND_DATA_OUT</b> defined in MtpExt.h to specify the size.This parameter cannot be <b>NULL</b>.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



This method provides a private mode of communication between the application and the service provider. The service provider can then process this IOCTL, optionally modify it, and pass it to the kernel mode driver.

Compared to <a href="https://msdn.microsoft.com/4554318b-497f-488f-a52f-a392b8fee992">IWMDMDevice::SendOpaqueCommand</a>, this method better aligns with the <b>DeviceIoControl</b> Windows API because the output buffer is supplied by the caller. Also, unlike <b>IWMDMDevice::SendOpaqueCommand</b>, this method does not involve any MAC check and is more efficient.

This method can be used, for example, to send custom Media Transport Protocol (MTP) commands to an MTP device.




## -see-also




<a href="https://msdn.microsoft.com/29e0ec95-c1ea-4157-b5aa-39d80fff407d">IWMDMDevice3 Interface</a>



<a href="https://msdn.microsoft.com/4554318b-497f-488f-a52f-a392b8fee992">IWMDMDevice::SendOpaqueCommand</a>
 

 

