---
UID: NI:genericusbfnioctl.IOCTL_GENERICUSBFN_TRANSFER_IN
title: IOCTL_GENERICUSBFN_TRANSFER_IN
author: windows-driver-content
description: This I/O control code (IOCTL) is sent by a user-mode service or application to issue an IN direction transfer on the endpoint that corresponds to the specified pipe ID in the input buffer.
old-location: buses\ioctl_genericusbfn_transfer_in.htm
old-project: usbref
ms.assetid: 70F78F02-6413-445F-9B5A-F70ADA741889
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: IOCTL_GENERICUSBFN_TRANSFER_IN, IOCTL_GENERICUSBFN_TRANSFER_IN control code [Buses], buses.ioctl_genericusbfn_transfer_in, genericusbfnioctl/IOCTL_GENERICUSBFN_TRANSFER_IN
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: genericusbfnioctl.h
req.include-header: GenericUsbFnIoctl.h
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	GenericUsbFnIoctl.h
api_name:
-	IOCTL_GENERICUSBFN_TRANSFER_IN
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IOCTL_GENERICUSBFN_TRANSFER_IN IOCTL


## -description



This  I/O control code (IOCTL) is sent by a user-mode service or application to issue  an IN direction transfer on the endpoint that corresponds to the specified pipe ID in the input buffer. 




## -ioctlparameters




### -input-buffer

A <b>USBFNPIPEID</b> that specifies the ID of the pipe to conduct the transfer on.


### -input-buffer-length

The size of a <b>USBFNPIPEID</b>.


### -output-buffer

The data to send to the host. From the host perspective the data is sent from the IN direction, representing an outbound transfer from the device to the host.


### -output-buffer-length

The size of the output buffer in bytes.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

<b>Irp-&gt;IoStatus.Status</b> is set to STATUS_SUCCESS if the request is successful. Otherwise, <b>Status</b> to the appropriate error condition as a <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> code. 


## -remarks



If this I/O control code (IOCTL) is being called synchronously, set the <i>lpOverlapped</i> parameter to NULL. If this IOCTL is called asynchronously, assign the <i>lpOverlapped</i> parameter to a pointer to an <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure that contains a handle to an event object. The event objects signal when the operation is completed.

The return value is a BOOL value that indicates success or failure of the operation. TRUE indicates success, FALSE otherwise.




## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt187881">IOCTL_GENERICUSBFN_TRANSFER_IN_APPEND_ZERO_PKT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt187882">IOCTL_GENERICUSBFN_TRANSFER_OUT</a>
 

 

