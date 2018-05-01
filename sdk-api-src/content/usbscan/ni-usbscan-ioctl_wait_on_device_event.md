---
UID: NI:usbscan.IOCTL_WAIT_ON_DEVICE_EVENT
title: IOCTL_WAIT_ON_DEVICE_EVENT
author: windows-driver-content
description: Returns information about an event occurring on a USB interrupt pipe.
old-location: image\ioctl_wait_on_device_event.htm
old-project: image
ms.assetid: 0895a19b-bb28-405a-98df-28522a18ec2b
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IOCTL_WAIT_ON_DEVICE_EVENT, IOCTL_WAIT_ON_DEVICE_EVENT control code [Imaging Devices], image.ioctl_wait_on_device_event, stifnc_ef4b6e5f-ed60-4354-adae-443e1a27b215.xml, usbscan/IOCTL_WAIT_ON_DEVICE_EVENT
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
-	IOCTL_WAIT_ON_DEVICE_EVENT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IOCTL_WAIT_ON_DEVICE_EVENT IOCTL


## -description


Returns information about an event occurring on a USB interrupt pipe.


## -ioctlparameters




### -input-buffer

<b>NULL</b>


### -input-buffer-length

Zero.


### -output-buffer

Pointer to a buffer that is large enough to receive the largest packet the device is capable of sending on the interrupt pipe.


### -output-buffer-length

Size of the output buffer.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

<b>Irp-&gt;IoStatus.Status</b> is set to STATUS_SUCCESS if the request is successful. Otherwise, <b>Status</b> to the appropriate error condition as a <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> code. 


## -remarks



<h3><a id="ddk_ioctl_wait_on_device_event_si"></a><a id="DDK_IOCTL_WAIT_ON_DEVICE_EVENT_SI"></a>DeviceIoControl Parameters</h3>


When the <b>DeviceloControl</b> function is called with the IOCTL_WAIT_ON_DEVICE_EVENT control code, the caller must specify a buffer pointer as the function's <i>lpOutBuffer</i> parameter. The buffer must be large enough to hold the largest packet the device can send on its interrupt pipe.

The type and size of information returned are device-specific. For example, a still image device might issue an interrupt when a user presses one of its buttons, and the return packet might indicate which button was pressed.

For more information, see <a href="https://msdn.microsoft.com/f9216d3c-4930-4c26-8eac-6ee500b038e0">Accessing Kernel-Mode Drivers for Still Image Devices</a>.



