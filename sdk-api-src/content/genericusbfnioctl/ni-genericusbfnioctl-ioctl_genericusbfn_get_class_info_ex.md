---
UID: NI:genericusbfnioctl.IOCTL_GENERICUSBFN_GET_CLASS_INFO_EX
title: IOCTL_GENERICUSBFN_GET_CLASS_INFO_EX
author: windows-sdk-content
description: This I/O control code (IOCTL) is sent by a user-mode service or application to retrieve information about a device's available pipes as configured in the registry.
old-location: buses\ioctl_genericusbfn_get_class_info_ex.htm
tech.root: usbref
ms.assetid: 9FC6E1F4-65AF-4315-B7F2-241E74820742
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: IOCTL_GENERICUSBFN_GET_CLASS_INFO_EX, IOCTL_GENERICUSBFN_GET_CLASS_INFO_EX control, IOCTL_GENERICUSBFN_GET_CLASS_INFO_EX control code [Buses], buses.ioctl_genericusbfn_get_class_info_ex, genericusbfnioctl/IOCTL_GENERICUSBFN_GET_CLASS_INFO_EX
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
 - IOCTL_GENERICUSBFN_GET_CLASS_INFO_EX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_GENERICUSBFN_GET_CLASS_INFO_EX IOCTL


## -description



This I/O control code (IOCTL) is sent by a  user-mode service or application to retrieve information about a device's available pipes as configured in the registry. 




## -ioctlparameters




### -input-buffer

NULL.


### -input-buffer-length

None.


### -output-buffer

A <a href="https://msdn.microsoft.com/373D7CA9-AF1B-46E8-AE6A-F693A9214527">USBFN_CLASS_INFORMATION_PACKET_EX</a> that provides information about the available pipes for a device.


### -output-buffer-length

The size of a <a href="https://msdn.microsoft.com/373D7CA9-AF1B-46E8-AE6A-F693A9214527">USBFN_CLASS_INFORMATION_PACKET_EX</a> structure.


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



<a href="https://msdn.microsoft.com/DF30E838-9C5A-45DD-8E51-5642CF726918">IOCTL_GENERICUSBFN_GET_CLASS_INFO</a>
 

 

