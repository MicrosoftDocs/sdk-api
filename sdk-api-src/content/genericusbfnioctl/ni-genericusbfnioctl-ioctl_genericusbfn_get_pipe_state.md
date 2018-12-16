---
UID: NI:genericusbfnioctl.IOCTL_GENERICUSBFN_GET_PIPE_STATE
title: IOCTL_GENERICUSBFN_GET_PIPE_STATE
author: windows-sdk-content
description: This I/O control code (IOCTL) is sent by a user-mode service or application to get the state of the specified Universal Serial Bus (USB) pipe.
old-location: buses\ioctl_genericusbfn_get_pipe_state.htm
tech.root: usbref
ms.assetid: AC0C24AF-F844-488B-A9E7-AE118C5E2F32
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IOCTL_GENERICUSBFN_GET_PIPE_STATE, IOCTL_GENERICUSBFN_GET_PIPE_STATE control, IOCTL_GENERICUSBFN_GET_PIPE_STATE control code [Buses], buses.ioctl_genericusbfn_get_pipe_state, genericusbfnioctl/IOCTL_GENERICUSBFN_GET_PIPE_STATE
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - GenericUsbFnIoctl.h
api_name:
 - IOCTL_GENERICUSBFN_GET_PIPE_STATE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_GENERICUSBFN_GET_PIPE_STATE IOCTL


## -description


This I/O control code (IOCTL) is sent by a user-mode service or application to get the state of the specified Universal Serial Bus (USB) pipe.


## -ioctlparameters




### -input-buffer

A <b>USBFNPIPEID</b> that specifies the ID of the pipe to retrieve state information for.


### -input-buffer-length

The size of a <b>USBFNPIPEID</b>.


### -output-buffer

Contains a BOOLEAN value that specifies whether the specified pipe is stalled. A value of TRUE if the specified pipe is stalled; FALSE if otherwise.


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



<a href="https://msdn.microsoft.com/C9276A60-382C-40FE-B5B9-49E95C71CDE9">IOCTL_GENERICUSBFN_SET_PIPE_STATE</a>
 

 

