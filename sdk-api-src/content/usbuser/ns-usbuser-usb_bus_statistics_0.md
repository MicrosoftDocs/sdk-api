---
UID: NS:usbuser._USB_BUS_STATISTICS_0
title: USB_BUS_STATISTICS_0 (usbuser.h)
description: The USB_BUS_STATISTICS_0 structure is used with the IOCTL_USB_USER_REQUEST I/O control request to retrieve bus statistics.
helpviewer_keywords: ["*PUSB_BUS_STATISTICS_0","PUSB_BUS_STATISTICS_0","PUSB_BUS_STATISTICS_0 structure pointer [Buses]","USB_BUS_STATISTICS_0","USB_BUS_STATISTICS_0 structure [Buses]","buses.usb_bus_statistics_0","usbstrct_673e06da-582e-4496-9f33-b0c8b915ef0f.xml","usbuser/PUSB_BUS_STATISTICS_0","usbuser/USB_BUS_STATISTICS_0"]
old-location: buses\usb_bus_statistics_0.htm
tech.root: buses
ms.assetid: d9673718-c39c-4f26-8d59-553366b8bd0a
ms.date: 12/05/2018
ms.keywords: '*PUSB_BUS_STATISTICS_0, PUSB_BUS_STATISTICS_0, PUSB_BUS_STATISTICS_0 structure pointer [Buses], USB_BUS_STATISTICS_0, USB_BUS_STATISTICS_0 structure [Buses], buses.usb_bus_statistics_0, usbstrct_673e06da-582e-4496-9f33-b0c8b915ef0f.xml, usbuser/PUSB_BUS_STATISTICS_0, usbuser/USB_BUS_STATISTICS_0'
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
req.typenames: USB_BUS_STATISTICS_0, *PUSB_BUS_STATISTICS_0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USB_BUS_STATISTICS_0
 - usbuser/_USB_BUS_STATISTICS_0
 - PUSB_BUS_STATISTICS_0
 - usbuser/PUSB_BUS_STATISTICS_0
 - USB_BUS_STATISTICS_0
 - usbuser/USB_BUS_STATISTICS_0
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
 - USB_BUS_STATISTICS_0
---

# USB_BUS_STATISTICS_0 structure


## -description

The <b>USB_BUS_STATISTICS_0</b> structure is used with the <a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a> I/O control request to retrieve bus statistics.

## -struct-fields

### -field DeviceCount

The number of devices on the bus.

### -field CurrentSystemTime

The current system time.

### -field CurrentUsbFrame

The number of the current USB frame.

### -field BulkBytes

The amount, in bytes, of bulk transfer data.

### -field IsoBytes

The amount, in bytes, of isochronous data.

### -field InterruptBytes

The amount, in bytes, of interrupt data.

### -field ControlDataBytes

The amount, in bytes, of control data.

### -field PciInterruptCount

The amount, in bytes, of interrupt data.

### -field HardResetCount

The number of hard bus resets that have occurred.

### -field WorkerSignalCount

The number of times that a worker thread has signaled completion of a task.

### -field CommonBufferBytes

The number of bytes that are transferred by common buffer.

### -field WorkerIdleTimeMs

The amount of time, in milliseconds, that worker threads have been idle.

### -field RootHubEnabled

A Boolean value that indicates whether the root hub is enabled. If <b>TRUE</b>, he root hub is enabled. If <b>FALSE</b>, the root hub is disabled.

### -field RootHubDevicePowerState

The power state of the root hub devices. This member can have any of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
0

</td>
<td>
D0 power state

</td>
</tr>
<tr>
<td>
1

</td>
<td>
D1 power state

</td>
</tr>
<tr>
<td>
2

</td>
<td>
D2 power state

</td>
</tr>
<tr>
<td>
3

</td>
<td>
D3 power state

</td>
</tr>
</table>

### -field Unused

If this member is 1, the bus is active. If 0, the bus is inactive.

### -field NameIndex

The index that is used to generate a symbolic link name for the hub PDO. This format of the symbolic link is USBPDO-<i>n</i>, where <i>n</i> is the value in <b>NameIndex</b>.

## -remarks

The <b>USB_BUS_STATISTICS_0</b> structure is used with the <a href="/windows/desktop/api/usbuser/ns-usbuser-usbuser_bus_statistics_0_request">USBUSER_BUS_STATISTICS_0</a> user-mode request. For a description of this request, see <a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>.

In Windows 8, this request completes successfully. However, the values retrieved from the underlying USB 3.0 driver stack do not reflect actual  bus statistics.

## -see-also

<a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>



<a href="/windows-hardware/drivers/usbcon/winusb-functions-for-pipe-policy-modification">USB Structures</a>