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

# EngDeviceIoControl function


## -description


The <b>EngDeviceIoControl</b> function sends a control code to the specified video miniport driver, causing the device to perform the specified operation.


## -parameters




### -param hDevice [in]

Handle to the device that is to perform the operation.


### -param dwIoControlCode [in]

Specifies the control code for the operation. The I/O controls are listed and described in full in <a href="https://msdn.microsoft.com/library/windows/hardware/ff570515">Video Miniport Driver I/O Control Codes</a>.


### -param lpInBuffer [in, optional]

Pointer to a buffer containing data required to perform the operation. This parameter can be <b>NULL</b> if the control code specifies an operation that does not require input data.


### -param nInBufferSize [in]

Specifies the size, in bytes, of <i>lpInBuffer</i>.


### -param lpOutBuffer [out, optional]

Pointer to a buffer in which the operation's output data is returned. This parameter can be <b>NULL</b> if the control code specifies an operation that does not produce output data.


### -param nOutBufferSize [in]

Specifies the size, in bytes, of <i>lpOutBuffer</i>.


### -param lpBytesReturned [out]

Pointer to a DWORD that specifies the actual size, in bytes, of the data returned in <i>lpOutBuffer</i>.


## -returns



The return value is a 32-bit Win32 API-defined error code.




## -remarks



<b>EngDeviceIoControl</b> is used by a display driver to communicate I/O requests to its corresponding miniport driver. This function provides the only communication channel between a display and video miniport driver.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff570547">VIDEO_REQUEST_PACKET</a>
 

 

