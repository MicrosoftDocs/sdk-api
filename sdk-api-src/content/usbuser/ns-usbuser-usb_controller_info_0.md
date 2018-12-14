---
UID: NS:usbuser._USB_CONTROLLER_INFO_0
title: USB_CONTROLLER_INFO_0
author: windows-sdk-content
description: The USB_CONTROLLER_INFO_0 structure is used with the IOCTL_USB_USER_REQUEST I/O control request to retrieve information about the USB host controller.
old-location: buses\usb_controller_info_0.htm
tech.root: usbref
ms.assetid: fcd88eb4-4fba-445a-b266-d89db8db1a55
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PUSB_CONTROLLER_INFO_0, PUSB_CONTROLLER_INFO_0, PUSB_CONTROLLER_INFO_0 structure pointer [Buses], USB_CONTROLLER_INFO_0, USB_CONTROLLER_INFO_0 structure [Buses], buses.usb_controller_info_0, usbstrct_2a3ac867-422b-46cf-b529-d1a9dde27970.xml, usbuser/PUSB_CONTROLLER_INFO_0, usbuser/USB_CONTROLLER_INFO_0"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: usbuser.h
req.include-header: Usbuser.h
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
 - usbuser.h
api_name:
 - USB_CONTROLLER_INFO_0
product: Windows
targetos: Windows
req.typenames: USB_CONTROLLER_INFO_0, *PUSB_CONTROLLER_INFO_0
req.redist: 
---

# USB_CONTROLLER_INFO_0 structure


## -description


The <b>USB_CONTROLLER_INFO_0</b> structure is used with the <a href="https://msdn.microsoft.com/6aba5cf4-a9fa-4d10-a212-acc79e00fa9b">IOCTL_USB_USER_REQUEST</a> I/O control request to retrieve information about the USB host controller.


## -struct-fields




### -field PciVendorId

The vendor identifier that is associated with the host controller device.


### -field PciDeviceId

The device identifier that is associated with the host controller.


### -field PciRevision

The revision number of the host controller device.


### -field NumberOfRootPorts

The number of root hub ports that the host controller has. 

<div class="alert"><b>Note</b>  In Windows 8, the USB 3.0 driver stack does not include the number of SuperSpeed hubs in the reported <b>NumberOfRootPorts</b> value.</div>
<div> </div>

### -field ControllerFlavor

A <a href="https://msdn.microsoft.com/c732fe90-50fb-4f6e-b42e-cb35c1ed0091">USB_CONTROLLER_FLAVOR</a>-typed enumerator  that specifies the type of controller.


### -field HcFeatureFlags

A bitwise OR of some combination of the following host controller feature flags.

<table>
<tr>
<th>Host controller feature</th>
<th>Meaning</th>
</tr>
<tr>
<td>
USB_HC_FEATURE_FLAG_PORT_POWER_SWITCHING

</td>
<td>
Power switching is enabled on the host controller. This flag allows powering of hot-plug devices.

</td>
</tr>
<tr>
<td>
USB_HC_FEATURE_FLAG_SEL_SUSPEND

</td>
<td>
Selective suspend is enabled on the host controller.

</td>
</tr>
<tr>
<td>
USB_HC_FEATURE_LEGACY_BIOS

</td>
<td>
The host controller has a legacy BIOS.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  In Windows 8, the underlying USB 3.0 driver stack does not set any host controller feature flags in <b>HcFeatureFlags.</b></div>
<div> </div>

## -remarks



The <b>USB_CONTROLLER_INFO_0</b> structure is used with the USBUSER_GET_CONTROLLER_INFO_0 user-mode request. For a description of this request, see <a href="https://msdn.microsoft.com/6aba5cf4-a9fa-4d10-a212-acc79e00fa9b">IOCTL_USB_USER_REQUEST</a>.




## -see-also




<a href="https://msdn.microsoft.com/6aba5cf4-a9fa-4d10-a212-acc79e00fa9b">IOCTL_USB_USER_REQUEST</a>



<a href="https://msdn.microsoft.com/c732fe90-50fb-4f6e-b42e-cb35c1ed0091">USB_CONTROLLER_FLAVOR</a>
 

 

