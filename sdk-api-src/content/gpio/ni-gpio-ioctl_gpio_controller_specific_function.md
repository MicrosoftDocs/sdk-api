---
UID: NI:gpio.IOCTL_GPIO_CONTROLLER_SPECIFIC_FUNCTION
title: IOCTL_GPIO_CONTROLLER_SPECIFIC_FUNCTION
author: windows-driver-content
description: The IOCTL_GPIO_CONTROLLER_SPECIFIC_FUNCTION I/O control code enables a client of the general-purpose I/O (GPIO) controller to request a controller-specific device-control operation.
old-location: gpio\ioctl_gpio_controller_specific_function.htm
old-project: GPIO
ms.assetid: 9B62BF0B-A172-4131-9196-590188C747AD
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GPIO.ioctl_gpio_controller_specific_function, IOCTL_GPIO_CONTROLLER_SPECIFIC_FUNCTION, IOCTL_GPIO_CONTROLLER_SPECIFIC_FUNCTION control code [Parallel Ports], gpio/IOCTL_GPIO_CONTROLLER_SPECIFIC_FUNCTION
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: gpio.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Supported starting with Windows 8.
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
req.typenames: GPOBROWSEINFO, *LPGPOBROWSEINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Gpio.h
api_name:
-	IOCTL_GPIO_CONTROLLER_SPECIFIC_FUNCTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IOCTL_GPIO_CONTROLLER_SPECIFIC_FUNCTION IOCTL


## -description


The <b>IOCTL_GPIO_CONTROLLER_SPECIFIC_FUNCTION</b> I/O control code enables a client of the general-purpose I/O (GPIO) controller to request a controller-specific device-control operation. Typically, the clients of a GPIO controller are drivers for peripheral devices that connect to GPIO pins.


## -ioctlparameters




### -input-buffer

The input buffer requirements for this I/O control code are defined by the developer of the GPIO controller driver. For more information about input buffers for METHOD_BUFFERED IRPs, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff540663">Buffer Descriptions for I/O Control Codes</a>.


### -input-buffer-length

TBD


### -output-buffer

The output buffer requirements for this I/O control code are defined by the developer of the GPIO controller driver. For more information about output buffers for METHOD_BUFFERED IRPs, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff540663">Buffer Descriptions for I/O Control Codes</a>.


### -output-buffer-length

TBD


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

If the operation is successful, the GPIO controller driver sets the <b>Status</b> member to STATUS_SUCCESS, and sets the <b>Information</b> member to the total number of bytes written to the output buffer. If an operation does not produce output data or the output data pointer is NULL, the <b>Information</b> member is set to zero.

If either the input buffer is not large enough to contain the input parameters or the output buffer is not large enough to contain the output parameters for the controller-specific operation, the <b>Status</b> member is set to STATUS_BUFFER_TOO_SMALL.

If this request fails, the <b>Status</b> member is set to an error code, and the <b>Information</b> member is set to zero.

If the GPIO controller driver does not any support controller-specific operations, the <b>Status</b> member is set to STATUS_NOT_IMPLEMENTED. If the GPIO controller driver supports controller-specific operations, but does not recognize the contents of the input buffer as valid, the <b>Status</b> member is set to STATUS_NOT_SUPPORTED.


## -remarks



Typical GPIO controllers do not support <b>IOCTL_GPIO_CONTROLLER_SPECIFIC_FUNCTION</b> requests. However, a controller driver developer has the option of defining one or more controller-specific operations to address the special requirements or capabilities of a GPIO controller on a particular hardware platform.

Only a peripheral device driver that is aware of the controller-specific operations supported by a particular type of GPIO controller hardware can use <b>IOCTL_GPIO_CONTROLLER_SPECIFIC_FUNCTION</b> requests to perform these operations. A peripheral device driver that uses these requests to perform controller-specific operations on one hardware platform risks the loss of compatibility with other platforms that do not support these operations.

The meaning of the <b>IOCTL_GPIO_CONTROLLER_SPECIFIC_FUNCTION</b> control code is defined by the developer of the GPIO controller driver. Typically, the controller driver uses this control code to enable peripheral device drivers to perform hardware-specific operations on the GPIO pins to which their devices are connected.

For example, the input buffer to the <b>IOCTL_GPIO_CONTROLLER_SPECIFIC_FUNCTION</b> request might contain a controller-defined command code and some number of input parameters. The GPIO controller driver may or may not write data to the output buffer, depending on the command code.

The peripheral device driver sends this I/O control request to the file object for the target GPIO device. The file object is a <a href="https://msdn.microsoft.com/library/windows/hardware/ff545834">FILE_OBJECT</a> structure that represents an open connection to a set of pins on the GPIO controller. Kernel-mode driver framework (KMDF) drivers use a WDFIOTARGET handle to refer to this file object. User-mode driver framework (UMDF) drivers access the file object through the <a href="https://msdn.microsoft.com/library/windows/hardware/ff560247">IWDFRemoteTarget</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545834">FILE_OBJECT</a>
 

 

