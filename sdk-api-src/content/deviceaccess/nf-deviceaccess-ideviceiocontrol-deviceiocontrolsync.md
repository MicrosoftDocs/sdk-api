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

# IDeviceIoControl::DeviceIoControlSync


## -description


The <b>DeviceIoControlSync</b> method sends a synchronous device input/output (I/O) control request to the device interface that the call to the <a href="https://msdn.microsoft.com/082d6297-20ac-4557-8205-0451482a5758">CreateDeviceAccessInstance</a> function specified.


## -parameters




### -param ioControlCode [in]

The I/O control code for the operation.


### -param inputBuffer [in]

An optional input buffer for the operation.


### -param inputBufferSize [in]

The size of input buffer, in bytes.


### -param outputBuffer [out]

An optional output buffer for the operation.


### -param outputBufferSize [in]

The size of output buffer, in bytes.


### -param bytesReturned [out]

A pointer to a variable that receives the number of bytes that were written into the output buffer, if one was specified.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Because  this is a synchronous method, you must not use it on a thread that can't handle being blocked for an extended period. In this case, you use the <b>DeviceIoControlAsync</b> method.




## -see-also




<a href="https://msdn.microsoft.com/d285e04e-04d0-4c2a-b9f0-72eebebf4f4b">IDeviceIoControl</a>
 

 

