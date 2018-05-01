---
UID: NS:usbscan._IO_BLOCK_EX
title: "_IO_BLOCK_EX"
author: windows-driver-content
description: The IO_BLOCK_EX structure is used as a parameter to DeviceIoControl, when the specified I/O control code is IOCTL_SEND_USB_REQUEST.
old-location: image\io_block_ex.htm
old-project: image
ms.assetid: 2474a49b-e275-4b4d-b762-c296b92bab4c
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: "*PIO_BLOCK_EX, IO_BLOCK_EX, IO_BLOCK_EX structure [Imaging Devices], PIO_BLOCK_EX, PIO_BLOCK_EX structure pointer [Imaging Devices], _IO_BLOCK_EX, image.io_block_ex, stifnc_6b21356d-4f1a-4b8d-a54e-767f46e5b1b3.xml, usbscan/IO_BLOCK_EX, usbscan/PIO_BLOCK_EX"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: usbscan.h
req.include-header: Usbscan.h
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
req.typenames: IO_BLOCK_EX, *PIO_BLOCK_EX
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	usbscan.h
api_name:
-	IO_BLOCK_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _IO_BLOCK_EX structure


## -description


The IO_BLOCK_EX structure is used as a parameter to <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>, when the specified I/O control code is <a href="https://msdn.microsoft.com/library/windows/hardware/ff542900">IOCTL_SEND_USB_REQUEST</a>. Values contained in structure members are used to create a USB Device Request (described in the <i>Universal Serial Bus Specification</i>).


## -struct-fields




### -field uOffset

Used as the <b>Value</b> field of a USB Device Request.


### -field uLength

Length of the buffer to transfer.


### -field pbyData

Pointer to a data buffer with a length of <b>uLength</b>.


### -field uIndex

Used as the <b>Index</b> field of a USB Device Request.


### -field bRequest

Used as the <b>bRequest</b> field of a USB Device Request.


### -field bmRequestType

Used as the <b>bmRequestType</b> field of a USB Device Request.


### -field fTransferDirectionIn

<b>TRUE</b> for transfers from device to host; <b>FALSE</b> for transfers from host to device.

