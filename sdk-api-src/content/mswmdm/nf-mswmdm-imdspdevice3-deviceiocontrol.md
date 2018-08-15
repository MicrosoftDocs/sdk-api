---
UID: NF:mswmdm.IMDSPDevice3.DeviceIoControl
title: IMDSPDevice3::DeviceIoControl
author: windows-sdk-content
description: The DeviceIoControl method calls the device I/O control.
old-location: wmdm\imdspdevice3_deviceiocontrol.htm
old-project: WMDM
ms.assetid: 1f41c3f9-8eb6-4d51-87f9-c8b035a73cce
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DeviceIoControl, DeviceIoControl method [windows Media Device Manager], DeviceIoControl method [windows Media Device Manager],IMDSPDevice3 interface, IMDSPDevice3 interface [windows Media Device Manager],DeviceIoControl method, IMDSPDevice3.DeviceIoControl, IMDSPDevice3::DeviceIoControl, IMDSPDevice3DeviceIoControl, mswmdm/IMDSPDevice3::DeviceIoControl, wmdm.imdspdevice3_deviceiocontrol
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IMDSPDevice3.DeviceIoControl
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMDSPDevice3::DeviceIoControl


## -description



The <b>DeviceIoControl</b> method calls the device I/O control.




## -parameters




### -param dwIoControlCode [in]

I/O control code being sent to the device.


### -param lpInBuffer [in]

Input buffer supplied by the calling application. This can be <b>NULL</b> if <i>nInBufferSize</i> is zero.


### -param nInBufferSize [in]

Size of <i>lpInBuffer</i>, in bytes.


### -param lpOutBuffer [out]

Output buffer, supplied by the calling application.


### -param pnOutBufferSize [in]

Size of <i>lpOutBuffer</i>, in bytes.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



This method provides a private mode of communication between the application and the service provider. The service provider can then process this IOCTL, optionally modify it, and pass it to the kernel-mode driver.

Compared to <a href="https://msdn.microsoft.com/d7b60187-84d1-4ff3-ab58-e6b8ea75ee37">IMDSPDevice::SendOpaqueCommand</a>, this method better aligns with the <b>DeviceIoControl</b> Windows API because the output buffer is supplied by the caller. Also, unlike <b>IMDSPDevice::SendOpaqueCommand</b>, this method does not involve any MAC check and is more efficient.




## -see-also




<a href="https://msdn.microsoft.com/919c26f4-6954-462a-8b4a-530e78bb72e6">IMDSPDevice3 Interface</a>



<a href="https://msdn.microsoft.com/d7b60187-84d1-4ff3-ab58-e6b8ea75ee37">IMDSPDevice::SendOpaqueCommand</a>



<a href="https://msdn.microsoft.com/3ef6a95d-d4e2-4608-9a02-98b497e1fdbb">IWMDMDevice3::DeviceIoControl</a>
 

 

