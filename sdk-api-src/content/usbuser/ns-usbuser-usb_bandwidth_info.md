---
UID: NS:usbuser._USB_BANDWIDTH_INFO
title: USB_BANDWIDTH_INFO (usbuser.h)
description: The USB_BANDWIDTH_INFO structure is used with the IOCTL_USB_USER_REQUEST I/O control request to retrieve information about the allocated bandwidth.
helpviewer_keywords: ["*PUSB_BANDWIDTH_INFO","PUSB_BANDWIDTH_INFO","PUSB_BANDWIDTH_INFO structure pointer [Buses]","USB_BANDWIDTH_INFO","USB_BANDWIDTH_INFO structure [Buses]","buses.usb_bandwidth_info","usbstrct_d852c165-11b3-405f-aa49-dc7f48f710a1.xml","usbuser/PUSB_BANDWIDTH_INFO","usbuser/USB_BANDWIDTH_INFO"]
old-location: buses\usb_bandwidth_info.htm
tech.root: buses
ms.assetid: 33983bed-9794-4deb-8d30-1089eee9eb9c
ms.date: 12/05/2018
ms.keywords: '*PUSB_BANDWIDTH_INFO, PUSB_BANDWIDTH_INFO, PUSB_BANDWIDTH_INFO structure pointer [Buses], USB_BANDWIDTH_INFO, USB_BANDWIDTH_INFO structure [Buses], buses.usb_bandwidth_info, usbstrct_d852c165-11b3-405f-aa49-dc7f48f710a1.xml, usbuser/PUSB_BANDWIDTH_INFO, usbuser/USB_BANDWIDTH_INFO'
req.header: usbuser.h
req.include-header: Usbuser.h
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
req.typenames: USB_BANDWIDTH_INFO, *PUSB_BANDWIDTH_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USB_BANDWIDTH_INFO
 - usbuser/_USB_BANDWIDTH_INFO
 - PUSB_BANDWIDTH_INFO
 - usbuser/PUSB_BANDWIDTH_INFO
 - USB_BANDWIDTH_INFO
 - usbuser/USB_BANDWIDTH_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - usbuser.h
api_name:
 - USB_BANDWIDTH_INFO
---

# USB_BANDWIDTH_INFO structure


## -description

The <b>USB_BANDWIDTH_INFO</b> structure is used with the <a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a> I/O control request to retrieve information about the allocated bandwidth.

## -struct-fields

### -field DeviceCount

The number of devices on the bus.

### -field TotalBusBandwidth

The amount of allocated bandwidth, in bits per millisecond.

### -field Total32secBandwidth

The amount of allocated bandwidth bits in each 32-millisecond time slice.

### -field AllocedBulkAndControl

The amount of bandwidth, in bits per 32-millisecond, that is allocated for bulk and control transfers.

### -field AllocedIso

The amount of bandwidth, in bits per 32-millisecond, that is allocated for isochronous transfers.

### -field AllocedInterrupt_1ms

The amount of bandwidth, in bits per 32-millisecond, that is allocated for interrupt transactions when the period is 1 millisecond.

### -field AllocedInterrupt_2ms

The amount of bandwidth, in bits per 32-millisecond, that is allocated for interrupt transactions when the period is 2 milliseconds.

### -field AllocedInterrupt_4ms

The amount of bandwidth, in bits per 32-millisecond, that is allocated for interrupt transactions when the period is 4 milliseconds.

### -field AllocedInterrupt_8ms

The amount of bandwidth, in bits per 32-millisecond, that is allocated for interrupt transactions when the period is 8 milliseconds.

### -field AllocedInterrupt_16ms

The amount of bandwidth, in bits per 32-millisecond, that is allocated for interrupt transactions when the period is 16 milliseconds.

### -field AllocedInterrupt_32ms

The amount of bandwidth, in bits per 32-millisecond, that is allocated for interrupt transactions when the period is 32 milliseconds.

## -remarks

The <b>USB_BANDWIDTH_INFO</b> structure is used with the USBUSER_GET_BANDWIDTH_INFORMATION user-mode request. For a description of this request, see <a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>.

In Windows 8, this request completes successfully. However, the values retrieved from the underlying USB 3.0 driver stack do not reflect actual information about the allocated bandwidth. That is because the bandwidth information is not exposed by xHCI controllers.

## -see-also

<a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>



<a href="/windows-hardware/drivers/ddi/content/index">USB Structures</a>