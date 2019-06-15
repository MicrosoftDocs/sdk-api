---
UID: NS:winusbio._WINUSB_PIPE_INFORMATION_EX
title: WINUSB_PIPE_INFORMATION_EX (winusbio.h)
author: windows-sdk-content
description: The WINUSB_PIPE_INFORMATION_EX structure contains pipe information that the WinUsb_QueryPipeEx routine retrieves.
old-location: buses\win_usb_pipe_information_ex.htm
tech.root: usbref
ms.assetid: 1A70E67D-8A1E-4041-A1E4-E322317E2849
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PWINUSB_PIPE_INFORMATION_EX, PWINUSB_PIPE_INFORMATION_EX, PWINUSB_PIPE_INFORMATION_EX structure pointer [Buses], WINUSB_PIPE_INFORMATION_EX, WINUSB_PIPE_INFORMATION_EX structure [Buses], buses.win_usb_pipe_information_ex, winusbio/PWINUSB_PIPE_INFORMATION_EX, winusbio/WINUSB_PIPE_INFORMATION_EX"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winusbio.h
api_name:
 - WINUSB_PIPE_INFORMATION_EX
product: Windows
targetos: Windows
req.typenames: WINUSB_PIPE_INFORMATION_EX, *PWINUSB_PIPE_INFORMATION_EX
req.redist: 
ms.custom: 19H1
---

# WINUSB_PIPE_INFORMATION_EX structure


## -description


The <b>WINUSB_PIPE_INFORMATION_EX</b> structure contains pipe information that the <a href="https://docs.microsoft.com/windows/desktop/api/winusb/nf-winusb-winusb_querypipeex">WinUsb_QueryPipeEx</a> routine retrieves.


## -struct-fields




### -field PipeType

A <a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/usb/ne-usb-_usbd_pipe_type">USBD_PIPE_TYPE</a>-type enumeration value that specifies the pipe type.


### -field PipeId

The pipe identifier (ID).


### -field MaximumPacketSize

The maximum size, in bytes, of the packets that are transmitted on the pipe.


### -field Interval

The pipe interval.


### -field MaximumBytesPerInterval

The maximum number of bytes that can be transmitted in single interval.  This value may be a larger than the <b>MaximumPacketSize</b> value on high-bandwidth, high-speed periodic endpoints and SuperSpeed periodic endpoints, such as isochronous endpoints.


## -see-also




<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/index">USB Structures</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/usb/ne-usb-_usbd_pipe_type">USBD_PIPE_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winusb/nf-winusb-winusb_querypipe">WinUsb_QueryPipe</a>
 

 

