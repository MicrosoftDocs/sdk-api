---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



This method provides a private mode of communication between the application and the service provider. The service provider can then process this IOCTL, optionally modify it, and pass it to the kernel-mode driver.

Compared to <a href="https://msdn.microsoft.com/d7b60187-84d1-4ff3-ab58-e6b8ea75ee37">IMDSPDevice::SendOpaqueCommand</a>, this method better aligns with the <b>DeviceIoControl</b> Windows API because the output buffer is supplied by the caller. Also, unlike <b>IMDSPDevice::SendOpaqueCommand</b>, this method does not involve any MAC check and is more efficient.




## -see-also




<a href="https://msdn.microsoft.com/919c26f4-6954-462a-8b4a-530e78bb72e6">IMDSPDevice3 Interface</a>



<a href="https://msdn.microsoft.com/d7b60187-84d1-4ff3-ab58-e6b8ea75ee37">IMDSPDevice::SendOpaqueCommand</a>



<a href="https://msdn.microsoft.com/3ef6a95d-d4e2-4608-9a02-98b497e1fdbb">IWMDMDevice3::DeviceIoControl</a>
 

 

