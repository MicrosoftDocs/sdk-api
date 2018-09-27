---
UID: NS:usbuser._USB_BUS_STATISTICS_0
title: "_USB_BUS_STATISTICS_0"
author: windows-sdk-content
description: The USB_BUS_STATISTICS_0 structure is used with the IOCTL_USB_USER_REQUEST I/O control request to retrieve bus statistics.
old-location: buses\usb_bus_statistics_0.htm
tech.root: UsbRef
ms.assetid: d9673718-c39c-4f26-8d59-553366b8bd0a
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: "*PUSB_BUS_STATISTICS_0, PUSB_BUS_STATISTICS_0, PUSB_BUS_STATISTICS_0 structure pointer [Buses], USB_BUS_STATISTICS_0, USB_BUS_STATISTICS_0 structure [Buses], _USB_BUS_STATISTICS_0, buses.usb_bus_statistics_0, usbstrct_673e06da-582e-4496-9f33-b0c8b915ef0f.xml, usbuser/PUSB_BUS_STATISTICS_0, usbuser/USB_BUS_STATISTICS_0"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - usbuser.h
api_name:
 - USB_BUS_STATISTICS_0
product: Windows
targetos: Windows
req.typenames: USB_BUS_STATISTICS_0, *PUSB_BUS_STATISTICS_0
req.redist: 
---

# _USB_BUS_STATISTICS_0 structure


## -description


The <b>USB_BUS_STATISTICS_0</b> structure is used with the <a href="https://msdn.microsoft.com/6aba5cf4-a9fa-4d10-a212-acc79e00fa9b">IOCTL_USB_USER_REQUEST</a> I/O control request to retrieve bus statistics.


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



The <b>USB_BUS_STATISTICS_0</b> structure is used with the <a href="https://msdn.microsoft.com/9913bcf7-61ce-4d96-9510-3b8d2117a802">USBUSER_BUS_STATISTICS_0</a> user-mode request. For a description of this request, see <a href="https://msdn.microsoft.com/6aba5cf4-a9fa-4d10-a212-acc79e00fa9b">IOCTL_USB_USER_REQUEST</a>.

In Windows 8, this request completes successfully. However, the values retrieved from the underlying USB 3.0 driver stack do not reflect actual  bus statistics.




## -see-also




<a href="https://msdn.microsoft.com/6aba5cf4-a9fa-4d10-a212-acc79e00fa9b">IOCTL_USB_USER_REQUEST</a>



<a href="https://msdn.microsoft.com/8ca7033d-6586-4c34-b940-67ddfbe21af9">USB Structures</a>
 

 

