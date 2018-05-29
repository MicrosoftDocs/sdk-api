---
UID: NS:winusbio._WINUSB_PIPE_INFORMATION
title: "_WINUSB_PIPE_INFORMATION"
author: windows-sdk-content
description: The WINUSB_PIPE_INFORMATION structure contains pipe information that the WinUsb_QueryPipe routine retrieves.
old-location: buses\winusb_pipe_information.htm
old-project: usbref
ms.assetid: 59e1d5e3-8c42-4f2f-b9a4-c637206d5494
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: "*PWINUSB_PIPE_INFORMATION, PWINUSB_PIPE_INFORMATION, PWINUSB_PIPE_INFORMATION structure pointer [Buses], WINUSB_PIPE_INFORMATION, WINUSB_PIPE_INFORMATION structure [Buses], _WINUSB_PIPE_INFORMATION, buses.winusb_pipe_information, usbstrct_7d5b5dff-05a6-4902-a8b6-6c913755c6a5.xml, winusbio/PWINUSB_PIPE_INFORMATION, winusbio/WINUSB_PIPE_INFORMATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winusbio.h
req.include-header: Winusbio.h
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
req.typenames: WINUSB_PIPE_INFORMATION, *PWINUSB_PIPE_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winusbio.h
api_name:
-	WINUSB_PIPE_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

