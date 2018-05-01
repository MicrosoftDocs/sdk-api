---
UID: NI:scsiscan.IOCTL_SCSISCAN_SET_TIMEOUT
title: IOCTL_SCSISCAN_SET_TIMEOUT
author: windows-driver-content
description: The IOCTL_SCSISCAN_SET_TIMEOUT control code modifies the time-out value used by the kernel-mode still image driver for SCSI buses when it accesses a device.
old-location: image\ioctl_scsiscan_set_timeout.htm
old-project: image
ms.assetid: 987816b3-ea5f-4689-b81f-f6d3328516c4
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IOCTL_SCSISCAN_SET_TIMEOUT, IOCTL_SCSISCAN_SET_TIMEOUT control code [Imaging Devices], image.ioctl_scsiscan_set_timeout, scsiscan/IOCTL_SCSISCAN_SET_TIMEOUT, stifnc_2b449c8c-c9b5-4f5a-be93-7efc1d8610bc.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: scsiscan.h
req.include-header: Scsiscan.h
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
req.typenames: SCHEDULE_HEADER, *PSCHEDULE_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	scsiscan.h
api_name:
-	IOCTL_SCSISCAN_SET_TIMEOUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOCTL_SCSISCAN_SET_TIMEOUT IOCTL


## -description


The <b>IOCTL_SCSISCAN_SET_TIMEOUT</b> control code modifies the time-out value used by the kernel-mode still image driver for SCSI buses when it accesses a device.


## -ioctlparameters




### -input-buffer

The location containing a time-out value, in half seconds.


### -input-buffer-length

Size of the input buffer


### -output-buffer

Set to NULL.


### -output-buffer-length

Set to 0.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

<b>Irp-&gt;IoStatus.Status</b> is set to STATUS_SUCCESS if the request is successful. Otherwise, <b>Status</b> to the appropriate error condition as a <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> code. 


## -remarks



When the kernel-mode SCSI still image driver sends a SCSI command to a device, by default the driver waits 30 seconds before timing out the operation. You can change the time-out value for a device by calling the <b>DeviceloControl</b> function with the <a href="https://msdn.microsoft.com/library/windows/hardware/ff542877">IOCTL_SCSISCAN_CMD</a> control code. The specified time-out value stays in effect until the device is closed.

Time-out values are specified in half seconds. Thus a specified value of 100 causes the driver to wait 50 seconds before timing out the device.

For more information, see <a href="https://msdn.microsoft.com/f9216d3c-4930-4c26-8eac-6ee500b038e0">Accessing Kernel-Mode Drivers for Still Image Devices</a>.

<b>Code example</b>

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>ULONG timeout = 240;
fRet = DeviceIoControl( m_DeviceDataHandle,
        (DWORD)IOCTL_SCSISCAN_SET_TIMEOUT,
        &amp;timeout,
        sizeof(ULONG),
        NULL, NULL, &amp;dwBytesReturned, NULL);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff542894">Creating IOCTL Requests in Drivers</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548651">WdfIoTargetSendInternalIoctlOthersSynchronously</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548656">WdfIoTargetSendInternalIoctlSynchronously</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548660">WdfIoTargetSendIoctlSynchronously</a>
 

 

