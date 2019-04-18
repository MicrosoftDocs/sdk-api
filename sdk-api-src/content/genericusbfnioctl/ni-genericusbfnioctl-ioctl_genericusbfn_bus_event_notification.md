---
UID: NI:genericusbfnioctl.IOCTL_GENERICUSBFN_BUS_EVENT_NOTIFICATION
title: IOCTL_GENERICUSBFN_BUS_EVENT_NOTIFICATION (genericusbfnioctl.h)
author: windows-sdk-content
description: This I/O control code (IOCTL) is sent by a user-mode service or application to register for Universal Serial Bus (USB) event.
old-location: buses\ioctl_genericusbfn_bus_event_notification.htm
tech.root: usbref
ms.assetid: 1DFDF22D-D86D-4875-B11D-45C0577B6281
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOCTL_GENERICUSBFN_BUS_EVENT_NOTIFICATION, IOCTL_GENERICUSBFN_BUS_EVENT_NOTIFICATION control, IOCTL_GENERICUSBFN_BUS_EVENT_NOTIFICATION control code [Buses], buses.ioctl_genericusbfn_bus_event_notification, genericusbfnioctl/IOCTL_GENERICUSBFN_BUS_EVENT_NOTIFICATION
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
 - IOCTL_GENERICUSBFN_BUS_EVENT_NOTIFICATION
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOCTL_GENERICUSBFN_BUS_EVENT_NOTIFICATION IOCTL


## -description


This  I/O control code (IOCTL) is sent by a user-mode  service or application to register for Universal Serial Bus (USB) event. After this request completes, notifications about events  such as a change in the port type or the receipt of a non-standard setup packet can be received. The <b>USBFN_NOTIFICATION</b> structure contained in the output buffer specifies which event has occurred and any associated data.


## -ioctlparameters




### -input-buffer

NULL.


### -input-buffer-length

None.


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
 

 

