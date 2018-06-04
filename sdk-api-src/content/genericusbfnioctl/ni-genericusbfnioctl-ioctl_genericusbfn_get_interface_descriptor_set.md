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

# IOCTL_GENERICUSBFN_GET_INTERFACE_DESCRIPTOR_SET IOCTL


## -description



This I/O control code (IOCTL) is sent by a user-mode service or application to get the entire Universal Serial Bus (USB) interface descriptor set for a function on the device.<div class="alert"><b>Note</b>  This IOCTL request does not retrieve the interface descriptor set for the entire device.</div>
<div> </div>





## -ioctlparameters




### -input-buffer

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/mt187998">USBFN_INTERFACE_INFO</a> structure.


### -input-buffer-length

The size of a <a href="https://msdn.microsoft.com/library/windows/hardware/mt187998">USBFN_INTERFACE_INFO</a> structure.


### -output-buffer

A pointer to a buffer that contains a <a href="https://msdn.microsoft.com/library/windows/hardware/mt187998">USBFN_INTERFACE_INFO</a> structure. The USB function class extension (UFX) populates the structure with the entire interface descriptor set including its endpoint descriptors.


### -output-buffer-length

The size of a <a href="https://msdn.microsoft.com/library/windows/hardware/mt187998">USBFN_INTERFACE_INFO</a>.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

<b>Irp-&gt;IoStatus.Status</b> is set to STATUS_SUCCESS if the request is successful. Otherwise, <b>Status</b> to the appropriate error condition as a <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> code. 


## -remarks



This request must be sent after sending the <a href="https://msdn.microsoft.com/library/windows/hardware/mt187868">IOCTL_GENERICUSBFN_ACTIVATE_USB_BUS</a> request.

The length of the entire interface descriptor is variable. The class driver might need to send this IOCTL request twice to get the entire descriptor set.

If the length of the entire descriptor set is greater than the  specified output buffer length, UFX sets the <b>Size</b> member of <a href="https://msdn.microsoft.com/library/windows/hardware/mt187998">USBFN_INTERFACE_INFO</a> to the actual buffer length and fails the request with STATUS_BUFFER_TOO_SMALL. The driver must then allocated an output buffer of length specified by <b>Size</b> and resend the request. 

If this I/O control code (IOCTL) is being called synchronously, set the <i>lpOverlapped</i> parameter to NULL. If this IOCTL is called asynchronously, assign the <i>lpOverlapped</i> parameter to a pointer to an <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure that contains a handle to an event object. The event objects signal when the operation is completed.

The return value is a BOOL value that indicates success or failure of the operation. TRUE indicates success, FALSE otherwise.




## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>
 

 

