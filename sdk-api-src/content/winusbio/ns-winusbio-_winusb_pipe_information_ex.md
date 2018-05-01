---
UID: NS:winusbio._WINUSB_PIPE_INFORMATION_EX
title: "_WINUSB_PIPE_INFORMATION_EX"
author: windows-driver-content
description: The WINUSB_PIPE_INFORMATION_EX structure contains pipe information that the WinUsb_QueryPipeEx routine retrieves.
old-location: buses\win_usb_pipe_information_ex.htm
old-project: usbref
ms.assetid: 1A70E67D-8A1E-4041-A1E4-E322317E2849
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: "*PWINUSB_PIPE_INFORMATION_EX, PWINUSB_PIPE_INFORMATION_EX, PWINUSB_PIPE_INFORMATION_EX structure pointer [Buses], WINUSB_PIPE_INFORMATION_EX, WINUSB_PIPE_INFORMATION_EX structure [Buses], _WINUSB_PIPE_INFORMATION_EX, buses.win_usb_pipe_information_ex, winusbio/PWINUSB_PIPE_INFORMATION_EX, winusbio/WINUSB_PIPE_INFORMATION_EX"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WINUSB_PIPE_INFORMATION_EX, *PWINUSB_PIPE_INFORMATION_EX
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winusbio.h
api_name:
-	WINUSB_PIPE_INFORMATION_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WINUSB_PIPE_INFORMATION_EX structure


## -description


The <b>WINUSB_PIPE_INFORMATION_EX</b> structure contains pipe information that the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265563">WinUsb_QueryPipeEx</a> routine retrieves.


## -struct-fields




### -field PipeType

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff539119">USBD_PIPE_TYPE</a>-type enumeration value that specifies the pipe type.


### -field PipeId

The pipe identifier (ID).


### -field MaximumPacketSize

The maximum size, in bytes, of the packets that are transmitted on the pipe.


### -field Interval

The pipe interval.


### -field MaximumBytesPerInterval

The maximum number of bytes that can be transmitted in single interval.  This value may be a larger than the <b>MaximumPacketSize</b> value on high-bandwidth, high-speed periodic endpoints and SuperSpeed periodic endpoints, such as isochronous endpoints.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff540160">USB Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539119">USBD_PIPE_TYPE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540293">WinUsb_QueryPipe</a>
 

 

