---
UID: NE:usbuser._WDMUSB_POWER_STATE
title: WDMUSB_POWER_STATE (usbuser.h)
description: The WDMUSB_POWER_STATE enumeration indicates the power state of a host controller or root hub.
helpviewer_keywords: ["WDMUSB_POWER_STATE","WDMUSB_POWER_STATE enumeration [Buses]","WdmUsbPowerDeviceD0","WdmUsbPowerDeviceD1","WdmUsbPowerDeviceD2","WdmUsbPowerDeviceD3","WdmUsbPowerDeviceUnspecified","WdmUsbPowerNotMapped","WdmUsbPowerSystemHibernate","WdmUsbPowerSystemShutdown","WdmUsbPowerSystemSleeping1","WdmUsbPowerSystemSleeping2","WdmUsbPowerSystemSleeping3","WdmUsbPowerSystemUnspecified","WdmUsbPowerSystemWorking","buses.wdmusb_power_state","usbstrct_fa696b93-8427-4480-b808-d02628a87f84.xml","usbuser/WDMUSB_POWER_STATE","usbuser/WdmUsbPowerDeviceD0","usbuser/WdmUsbPowerDeviceD1","usbuser/WdmUsbPowerDeviceD2","usbuser/WdmUsbPowerDeviceD3","usbuser/WdmUsbPowerDeviceUnspecified","usbuser/WdmUsbPowerNotMapped","usbuser/WdmUsbPowerSystemHibernate","usbuser/WdmUsbPowerSystemShutdown","usbuser/WdmUsbPowerSystemSleeping1","usbuser/WdmUsbPowerSystemSleeping2","usbuser/WdmUsbPowerSystemSleeping3","usbuser/WdmUsbPowerSystemUnspecified","usbuser/WdmUsbPowerSystemWorking"]
old-location: buses\wdmusb_power_state.htm
tech.root: buses
ms.assetid: 2f64bd5b-507c-4824-b50c-dbc228e8671a
ms.date: 12/05/2018
ms.keywords: WDMUSB_POWER_STATE, WDMUSB_POWER_STATE enumeration [Buses], WdmUsbPowerDeviceD0, WdmUsbPowerDeviceD1, WdmUsbPowerDeviceD2, WdmUsbPowerDeviceD3, WdmUsbPowerDeviceUnspecified, WdmUsbPowerNotMapped, WdmUsbPowerSystemHibernate, WdmUsbPowerSystemShutdown, WdmUsbPowerSystemSleeping1, WdmUsbPowerSystemSleeping2, WdmUsbPowerSystemSleeping3, WdmUsbPowerSystemUnspecified, WdmUsbPowerSystemWorking, buses.wdmusb_power_state, usbstrct_fa696b93-8427-4480-b808-d02628a87f84.xml, usbuser/WDMUSB_POWER_STATE, usbuser/WdmUsbPowerDeviceD0, usbuser/WdmUsbPowerDeviceD1, usbuser/WdmUsbPowerDeviceD2, usbuser/WdmUsbPowerDeviceD3, usbuser/WdmUsbPowerDeviceUnspecified, usbuser/WdmUsbPowerNotMapped, usbuser/WdmUsbPowerSystemHibernate, usbuser/WdmUsbPowerSystemShutdown, usbuser/WdmUsbPowerSystemSleeping1, usbuser/WdmUsbPowerSystemSleeping2, usbuser/WdmUsbPowerSystemSleeping3, usbuser/WdmUsbPowerSystemUnspecified, usbuser/WdmUsbPowerSystemWorking
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
req.typenames: WDMUSB_POWER_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WDMUSB_POWER_STATE
 - usbuser/_WDMUSB_POWER_STATE
 - WDMUSB_POWER_STATE
 - usbuser/WDMUSB_POWER_STATE
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
 - WDMUSB_POWER_STATE
---

# WDMUSB_POWER_STATE enumeration


## -description

The <b>WDMUSB_POWER_STATE</b> enumeration indicates the power state of a host controller or root hub.

## -enum-fields

### -field WdmUsbPowerNotMapped:0

Power state information is not mapped.

### -field WdmUsbPowerSystemUnspecified:100

Power state information is not available.

### -field WdmUsbPowerSystemWorking

The system is in the working state.

### -field WdmUsbPowerSystemSleeping1

The system is in the S1 power state.

### -field WdmUsbPowerSystemSleeping2

The system is in the S2 power state.

### -field WdmUsbPowerSystemSleeping3

The system is in the S3 power state.

### -field WdmUsbPowerSystemHibernate

The system is hibernating.

### -field WdmUsbPowerSystemShutdown

The system is shutdown.

### -field WdmUsbPowerDeviceUnspecified:200

A device is not specified.

### -field WdmUsbPowerDeviceD0

The host controller is in the D0 power state.

### -field WdmUsbPowerDeviceD1

The host controller is in the D1 power state.

### -field WdmUsbPowerDeviceD2

The host controller is in the D2 power state.

### -field WdmUsbPowerDeviceD3

The host controller is in the D3 power state.

## -remarks

The USB stack uses the <b>WDMUSB_POWER_STATE</b> enumeration to report the power state of the host controller after receiving a USBUSER_GET_POWER_STATE_MAP request. For more information about this request, see <a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>.

## -see-also

<a href="/windows/desktop/api/usbuser/ni-usbuser-ioctl_usb_user_request">IOCTL_USB_USER_REQUEST</a>



<a href="/windows-hardware/drivers/ddi/content/index">USB Constants and Enumerations</a>
