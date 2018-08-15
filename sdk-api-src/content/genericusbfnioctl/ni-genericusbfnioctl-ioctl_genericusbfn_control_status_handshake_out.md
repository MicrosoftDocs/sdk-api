---
UID: NI:genericusbfnioctl.IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_OUT
title: IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_OUT
author: windows-sdk-content
description: This I/O control code (IOCTL) is sent by a user-mode service or application to complete a zero-length control status handshake on endpoint 0 in the OUT direction.
old-location: buses\ioctl_genericusbfn_control_status_handshake_out.htm
old-project: usbref
ms.assetid: B8DE5F6E-6FC5-4E53-8A02-301A3CE436C9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_OUT, IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_OUT control, IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_OUT control code [Buses], buses.ioctl_genericusbfn_control_status_handshake_out, genericusbfnioctl/IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_OUT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: ioctl
req.header: genericusbfnioctl.h
req.include-header: GenericUsbFnIoctl.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - GenericUsbFnIoctl.h
api_name:
 - IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_OUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_OUT IOCTL


## -description



This   I/O control code (IOCTL) is sent by a user-mode service or application to complete  a zero-length control status handshake on endpoint 0 in the OUT direction.




## -ioctlparameters




### -input-buffer

A <b>USBFNPIPEID</b> that specifies the pipe ID of endpoint 0.


### -input-buffer-length

The size of a <b>USBFNPIPEID</b>.


### -output-buffer

NULL.


### -output-buffer-length

None.


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



<a href="https://msdn.microsoft.com/A01233F3-3C5F-4184-9AAA-7391BFD2EB02">IOCTL_GENERICUSBFN_CONTROL_STATUS_HANDSHAKE_IN</a>
 

 

