---
UID: NS:usbuser._USB_POWER_INFO
title: USB_POWER_INFO (usbuser.h)
description: The USB_POWER_INFO structure is used with the IOCTL_USB_USER_REQUEST I/O control request to retrieve device power state that the host controller power policy specifies for the indicated system power state.
helpviewer_keywords: ["*PUSB_POWER_INFO","PUSB_POWER_INFO","PUSB_POWER_INFO structure pointer [Buses]","USB_POWER_INFO","USB_POWER_INFO structure [Buses]","buses.usb_power_info","usbstrct_95ba66ea-20ee-4e05-8294-3b3bd06f7116.xml","usbuser/PUSB_POWER_INFO","usbuser/USB_POWER_INFO"]
old-location: buses\usb_power_info.htm
tech.root: buses
ms.assetid: b4f35d7e-b0e3-44d9-8e41-1752cb0af5ef
ms.date: 12/05/2018
ms.keywords: '*PUSB_POWER_INFO, PUSB_POWER_INFO, PUSB_POWER_INFO structure pointer [Buses], USB_POWER_INFO, USB_POWER_INFO structure [Buses], buses.usb_power_info, usbstrct_95ba66ea-20ee-4e05-8294-3b3bd06f7116.xml, usbuser/PUSB_POWER_INFO, usbuser/USB_POWER_INFO'
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
targetos: Windows
req.typenames: USB_POWER_INFO, *PUSB_POWER_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USB_POWER_INFO
 - usbuser/_USB_POWER_INFO
 - PUSB_POWER_INFO
 - usbuser/PUSB_POWER_INFO
 - USB_POWER_INFO
 - usbuser/USB_POWER_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - usbuser.h
api_name:
 - USB_POWER_INFO
---

# USB_POWER_INFO structure


## -description

The <b>USB_POWER_INFO</b> structure is used with the <a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a> I/O control request to retrieve device power state that the host controller power policy specifies for the indicated system power state.

## -struct-fields

### -field SystemState

On input, a <a href="/windows/desktop/api/usbuser/ne-usbuser-wdmusb_power_state">WDMUSB_POWER_STATE</a>-type enumerator value that specifies the system power state.

### -field HcDevicePowerState

On output, an <a href="/windows/desktop/api/usbuser/ne-usbuser-wdmusb_power_state">WDMUSB_POWER_STATE</a>-type enumerator value that specifies the device power state of the host controller.

### -field HcDeviceWake

On output, a <a href="/windows/desktop/api/usbuser/ne-usbuser-wdmusb_power_state">WDMUSB_POWER_STATE</a>-type enumerator value that specifies whether the host controller is in a wake state.

### -field HcSystemWake

On output, a <a href="/windows/desktop/api/usbuser/ne-usbuser-wdmusb_power_state">WDMUSB_POWER_STATE</a>-type enumerator value that specifies whether the host controller can wake the system.

### -field RhDevicePowerState

On output, a <a href="/windows/desktop/api/usbuser/ne-usbuser-wdmusb_power_state">WDMUSB_POWER_STATE</a>-type enumerator value that specifies the device power state of the root hub.

### -field RhDeviceWake

On output, a <a href="/windows/desktop/api/usbuser/ne-usbuser-wdmusb_power_state">WDMUSB_POWER_STATE</a>-type enumerator value that specifies whether the root hub is in a wake state.

### -field RhSystemWake

On output, a <a href="/windows/desktop/api/usbuser/ne-usbuser-wdmusb_power_state">WDMUSB_POWER_STATE</a>-type enumerator value that specifies whether the root hub can wake the system.

### -field LastSystemSleepState

On output, a <a href="/windows/desktop/api/usbuser/ne-usbuser-wdmusb_power_state">WDMUSB_POWER_STATE</a>-type enumerator value that specifies the last system sleep state.

### -field CanWakeup

A Boolean value that indicates whether the host controller device can wake up the system from the specified system power state. If <b>TRUE</b>, the host controller device can wake up the system. If <b>FALSE</b>, the host controller cannot wake up the system.

### -field IsPowered

A Boolean value that indicates whether the host controller is powered when in the specified system power state. If <b>TRUE</b>, the host controller is powered. If <b>FALSE</b>, the host controller is not powered.

## -remarks

The <b>USB_POWER_INFO</b> structure is used with the USBUSER_GET_POWER_STATE_MAP user-mode request. For more information about this request, see <a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>.

## -see-also

<a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>



<a href="/windows-hardware/drivers/ddi/content/index">USB Structures</a>