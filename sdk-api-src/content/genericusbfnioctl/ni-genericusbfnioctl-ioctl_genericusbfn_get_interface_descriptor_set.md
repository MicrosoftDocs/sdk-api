---
UID: NI:genericusbfnioctl.IOCTL_GENERICUSBFN_GET_INTERFACE_DESCRIPTOR_SET
title: IOCTL_GENERICUSBFN_GET_INTERFACE_DESCRIPTOR_SET
author: windows-sdk-content
description: This I/O control code (IOCTL) is sent by a user-mode service or application to get the entire interface descriptor set for a function on the device.This IOCTL request does not retrieve the interface descriptor set for the entire device.Universal Serial Bus (USB) interface descriptor set for a function on the device.
old-location: buses\ioctl_genericusbfn_get_interface_descriptor_set.htm
tech.root: UsbRef
ms.assetid: 35069739-1E73-4F60-A16C-26EFF5D33D55
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IOCTL_GENERICUSBFN_GET_INTERFACE_DESCRIPTOR_SET, IOCTL_GENERICUSBFN_GET_INTERFACE_DESCRIPTOR_SET control, IOCTL_GENERICUSBFN_GET_INTERFACE_DESCRIPTOR_SET control code [Buses], buses.ioctl_genericusbfn_get_interface_descriptor_set, genericusbfnioctl/IOCTL_GENERICUSBFN_GET_INTERFACE_DESCRIPTOR_SET
ms.prod: windows
ms.technology: windows-sdk
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
 - IOCTL_GENERICUSBFN_GET_INTERFACE_DESCRIPTOR_SET
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_GENERICUSBFN_GET_INTERFACE_DESCRIPTOR_SET IOCTL


## -description



This I/O control code (IOCTL) is sent by a user-mode service or application to get the entire Universal Serial Bus (USB) interface descriptor set for a function on the device.<div class="alert"><b>Note</b>  This IOCTL request does not retrieve the interface descriptor set for the entire device.</div>
<div> </div>





## -ioctlparameters




### -input-buffer

A pointer to a <a href="https://msdn.microsoft.com/54647A9E-E0AB-4DE7-93FB-D0232D6AC646">USBFN_INTERFACE_INFO</a> structure.


### -input-buffer-length

The size of a <a href="https://msdn.microsoft.com/54647A9E-E0AB-4DE7-93FB-D0232D6AC646">USBFN_INTERFACE_INFO</a> structure.


### -output-buffer

A pointer to a buffer that contains a <a href="https://msdn.microsoft.com/54647A9E-E0AB-4DE7-93FB-D0232D6AC646">USBFN_INTERFACE_INFO</a> structure. The USB function class extension (UFX) populates the structure with the entire interface descriptor set including its endpoint descriptors.


### -output-buffer-length

The size of a <a href="https://msdn.microsoft.com/54647A9E-E0AB-4DE7-93FB-D0232D6AC646">USBFN_INTERFACE_INFO</a>.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

<b>Irp-&gt;IoStatus.Status</b> is set to STATUS_SUCCESS if the request is successful. Otherwise, <b>Status</b> to the appropriate error condition as a <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> code. 


## -remarks



This request must be sent after sending the <a href="https://msdn.microsoft.com/A8CE2698-B2EF-409A-8251-7419F76D47BC">IOCTL_GENERICUSBFN_ACTIVATE_USB_BUS</a> request.

The length of the entire interface descriptor is variable. The class driver might need to send this IOCTL request twice to get the entire descriptor set.

If the length of the entire descriptor set is greater than the  specified output buffer length, UFX sets the <b>Size</b> member of <a href="https://msdn.microsoft.com/54647A9E-E0AB-4DE7-93FB-D0232D6AC646">USBFN_INTERFACE_INFO</a> to the actual buffer length and fails the request with STATUS_BUFFER_TOO_SMALL. The driver must then allocated an output buffer of length specified by <b>Size</b> and resend the request. 

If this I/O control code (IOCTL) is being called synchronously, set the <i>lpOverlapped</i> parameter to NULL. If this IOCTL is called asynchronously, assign the <i>lpOverlapped</i> parameter to a pointer to an <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure that contains a handle to an event object. The event objects signal when the operation is completed.

The return value is a BOOL value that indicates success or failure of the operation. TRUE indicates success, FALSE otherwise.




## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>
 

 

