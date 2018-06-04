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

# _USB_BUS_STATISTICS_0 structure


## -description


The <b>USB_BUS_STATISTICS_0</b> structure is used with the <a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a> I/O control request to retrieve bus statistics.


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



The <b>USB_BUS_STATISTICS_0</b> structure is used with the <a href="https://msdn.microsoft.com/9913bcf7-61ce-4d96-9510-3b8d2117a802">USBUSER_BUS_STATISTICS_0</a> user-mode request. For a description of this request, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a>.

In Windows 8, this request completes successfully. However, the values retrieved from the underlying USB 3.0 driver stack do not reflect actual  bus statistics.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540160">USB Structures</a>
 

 

