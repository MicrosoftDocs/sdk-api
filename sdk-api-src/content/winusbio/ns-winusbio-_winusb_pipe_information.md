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

# _WINUSB_PIPE_INFORMATION structure


## -description


The <b>WINUSB_PIPE_INFORMATION</b> structure contains pipe information that the <a href="https://msdn.microsoft.com/library/windows/hardware/ff540293">WinUsb_QueryPipe</a> routine retrieves.


## -struct-fields




### -field PipeType

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff539119">USBD_PIPE_TYPE</a>-type enumeration value that specifies the pipe type.


### -field PipeId

The pipe identifier (ID).


### -field MaximumPacketSize

The maximum size, in bytes, of the packets that are transmitted on the pipe.


### -field Interval

The pipe interval.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff540160">USB Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539119">USBD_PIPE_TYPE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540293">WinUsb_QueryPipe</a>
 

 

