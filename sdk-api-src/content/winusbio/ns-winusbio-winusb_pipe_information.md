---
UID: NS:winusbio._WINUSB_PIPE_INFORMATION
title: WINUSB_PIPE_INFORMATION (winusbio.h)
description: The WINUSB_PIPE_INFORMATION structure contains pipe information that the WinUsb_QueryPipe routine retrieves.
helpviewer_keywords: ["*PWINUSB_PIPE_INFORMATION","PWINUSB_PIPE_INFORMATION","PWINUSB_PIPE_INFORMATION structure pointer [Buses]","WINUSB_PIPE_INFORMATION","WINUSB_PIPE_INFORMATION structure [Buses]","buses.winusb_pipe_information","usbstrct_7d5b5dff-05a6-4902-a8b6-6c913755c6a5.xml","winusbio/PWINUSB_PIPE_INFORMATION","winusbio/WINUSB_PIPE_INFORMATION"]
old-location: buses\winusb_pipe_information.htm
tech.root: buses
ms.assetid: 59e1d5e3-8c42-4f2f-b9a4-c637206d5494
ms.date: 12/05/2018
ms.keywords: '*PWINUSB_PIPE_INFORMATION, PWINUSB_PIPE_INFORMATION, PWINUSB_PIPE_INFORMATION structure pointer [Buses], WINUSB_PIPE_INFORMATION, WINUSB_PIPE_INFORMATION structure [Buses], buses.winusb_pipe_information, usbstrct_7d5b5dff-05a6-4902-a8b6-6c913755c6a5.xml, winusbio/PWINUSB_PIPE_INFORMATION, winusbio/WINUSB_PIPE_INFORMATION'
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
targetos: Windows
req.typenames: WINUSB_PIPE_INFORMATION, *PWINUSB_PIPE_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WINUSB_PIPE_INFORMATION
 - winusbio/_WINUSB_PIPE_INFORMATION
 - PWINUSB_PIPE_INFORMATION
 - winusbio/PWINUSB_PIPE_INFORMATION
 - WINUSB_PIPE_INFORMATION
 - winusbio/WINUSB_PIPE_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winusbio.h
api_name:
 - WINUSB_PIPE_INFORMATION
---

# WINUSB_PIPE_INFORMATION structure


## -description

The <b>WINUSB_PIPE_INFORMATION</b> structure contains pipe information that the <a href="/windows/desktop/api/winusb/nf-winusb-winusb_querypipe">WinUsb_QueryPipe</a> routine retrieves.

## -struct-fields

### -field PipeType

A <a href="/windows-hardware/drivers/ddi/content/usb/ne-usb-_usbd_pipe_type">USBD_PIPE_TYPE</a>-type enumeration value that specifies the pipe type.

### -field PipeId

The pipe identifier (ID).

### -field MaximumPacketSize

The maximum size, in bytes, of the packets that are transmitted on the pipe.

### -field Interval

The pipe interval.

## -see-also

<a href="/windows-hardware/drivers/usbcon/winusb-functions-for-pipe-policy-modification">USB Structures</a>



<a href="/windows-hardware/drivers/ddi/content/usb/ne-usb-_usbd_pipe_type">USBD_PIPE_TYPE</a>



<a href="/windows/desktop/api/winusb/nf-winusb-winusb_querypipe">WinUsb_QueryPipe</a>