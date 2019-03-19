---
UID: NI:genericusbfnioctl.IOCTL_GENERICUSBFN_REGISTER_USB_STRING
title: IOCTL_GENERICUSBFN_REGISTER_USB_STRING (genericusbfnioctl.h)
author: windows-sdk-content
description: This I/O control code (IOCTL) is sent by a user-mode service or application to register a string descriptor.Universal Serial Bus (USB) string descriptor.
old-location: buses\ioctl_genericusbfn_register_usb_string.htm
tech.root: usbref
ms.assetid: E3BDD2EF-C3F2-435E-8473-84C8FFAEAB06
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IOCTL_GENERICUSBFN_REGISTER_USB_STRING, IOCTL_GENERICUSBFN_REGISTER_USB_STRING control, IOCTL_GENERICUSBFN_REGISTER_USB_STRING control code [Buses], buses.ioctl_genericusbfn_register_usb_string, genericusbfnioctl/IOCTL_GENERICUSBFN_REGISTER_USB_STRING
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
 - IOCTL_GENERICUSBFN_REGISTER_USB_STRING
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_GENERICUSBFN_REGISTER_USB_STRING IOCTL


## -description



This I/O control code (IOCTL) is sent by a user-mode service or application to register a Universal Serial Bus (USB) string descriptor.




## -ioctlparameters




### -input-buffer

A pointer to a buffer that contains a  <a href="https://msdn.microsoft.com/1169A369-0E6D-4308-ABF6-0724FED73AF9">USBFN_USB_STRING</a> structure with the USB string descriptor.


### -input-buffer-length

The size of a <a href="https://msdn.microsoft.com/1169A369-0E6D-4308-ABF6-0724FED73AF9">USBFN_USB_STRING</a> structure.


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



This request must be sent after sending the <a href="https://msdn.microsoft.com/A8CE2698-B2EF-409A-8251-7419F76D47BC">IOCTL_GENERICUSBFN_ACTIVATE_USB_BUS</a> request.

If this I/O control code (IOCTL) is being called synchronously, set the <i>lpOverlapped</i> parameter to NULL. If this IOCTL is called asynchronously, assign the <i>lpOverlapped</i> parameter to a pointer to an <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure that contains a handle to an event object. The event objects signal when the operation is completed.

The return value is a BOOL value that indicates success or failure of the operation. TRUE indicates success, FALSE otherwise.




## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>
 

 

