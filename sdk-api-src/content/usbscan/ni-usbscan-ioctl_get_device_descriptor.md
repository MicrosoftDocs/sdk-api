---
UID: NI:usbscan.IOCTL_GET_DEVICE_DESCRIPTOR
title: IOCTL_GET_DEVICE_DESCRIPTOR
author: windows-driver-content
description: Returns vendor and device identifiers.
old-location: image\ioctl_get_device_descriptor.htm
old-project: image
ms.assetid: a6946dd4-db72-477f-bf2c-958c363340a0
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IOCTL_GET_DEVICE_DESCRIPTOR, IOCTL_GET_DEVICE_DESCRIPTOR control code [Imaging Devices], image.ioctl_get_device_descriptor, stifnc_b84c2743-6548-40c7-8b97-4952867740ad.xml, usbscan/IOCTL_GET_DEVICE_DESCRIPTOR
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: usbscan.h
req.include-header: Usbscan.h
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
req.typenames: RAW_PIPE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Usbscan.h
api_name:
-	IOCTL_GET_DEVICE_DESCRIPTOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IOCTL_GET_DEVICE_DESCRIPTOR IOCTL


## -description


Returns vendor and device identifiers.


## -ioctlparameters




### -input-buffer

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff540576">DEVICE_DESCRIPTOR</a> structure.


### -input-buffer-length

Size of the input buffer.


### -output-buffer

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff540576">DEVICE_DESCRIPTOR</a> structure (same as <i>lpInbuffer</i>).


### -output-buffer-length

Size of the output buffer.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

<b>Irp-&gt;IoStatus.Status</b> is set to STATUS_SUCCESS if the request is successful. Otherwise, <b>Status</b> to the appropriate error condition as a <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> code. 


## -remarks



<h3><a id="ddk_ioctl_get_device_descriptor_si"></a><a id="DDK_IOCTL_GET_DEVICE_DESCRIPTOR_SI"></a>DeviceIoControl Parameters</h3>


When the <b>DeviceloControl</b> function is called with the IOCTL_GET_USB_DESCRIPTOR I/O control code, the caller must specify the address of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff540576">DEVICE_DESCRIPTOR</a> structure as the function's <i>lpOutbuffer</i> parameter. The kernel-mode driver fills in the structure.

For more information, see <a href="https://msdn.microsoft.com/f9216d3c-4930-4c26-8eac-6ee500b038e0">Accessing Kernel-Mode Drivers for Still Image Devices</a>.



