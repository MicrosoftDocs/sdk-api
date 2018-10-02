---
UID: NE:usbuser._WDMUSB_POWER_STATE
title: "_WDMUSB_POWER_STATE"
author: windows-sdk-content
description: The WDMUSB_POWER_STATE enumeration indicates the power state of a host controller or root hub.
old-location: buses\wdmusb_power_state.htm
tech.root: UsbRef
ms.assetid: 2f64bd5b-507c-4824-b50c-dbc228e8671a
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: WDMUSB_POWER_STATE, WDMUSB_POWER_STATE enumeration [Buses], WdmUsbPowerDeviceD0, WdmUsbPowerDeviceD1, WdmUsbPowerDeviceD2, WdmUsbPowerDeviceD3, WdmUsbPowerDeviceUnspecified, WdmUsbPowerNotMapped, WdmUsbPowerSystemHibernate, WdmUsbPowerSystemShutdown, WdmUsbPowerSystemSleeping1, WdmUsbPowerSystemSleeping2, WdmUsbPowerSystemSleeping3, WdmUsbPowerSystemUnspecified, WdmUsbPowerSystemWorking, _WDMUSB_POWER_STATE, buses.wdmusb_power_state, usbstrct_fa696b93-8427-4480-b808-d02628a87f84.xml, usbuser/WDMUSB_POWER_STATE, usbuser/WdmUsbPowerDeviceD0, usbuser/WdmUsbPowerDeviceD1, usbuser/WdmUsbPowerDeviceD2, usbuser/WdmUsbPowerDeviceD3, usbuser/WdmUsbPowerDeviceUnspecified, usbuser/WdmUsbPowerNotMapped, usbuser/WdmUsbPowerSystemHibernate, usbuser/WdmUsbPowerSystemShutdown, usbuser/WdmUsbPowerSystemSleeping1, usbuser/WdmUsbPowerSystemSleeping2, usbuser/WdmUsbPowerSystemSleeping3, usbuser/WdmUsbPowerSystemUnspecified, usbuser/WdmUsbPowerSystemWorking
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - WDMUSB_POWER_STATE
product: Windows
targetos: Windows
req.typenames: WDMUSB_POWER_STATE
req.redist: 
---

# _WDMUSB_POWER_STATE enumeration


## -description


The <b>WDMUSB_POWER_STATE</b> enumeration indicates the power state of a host controller or root hub.


## -enum-fields




### -field WdmUsbPowerNotMapped

Power state information is not mapped.


### -field WdmUsbPowerSystemUnspecified

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


### -field WdmUsbPowerDeviceUnspecified

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



The USB stack uses the <b>WDMUSB_POWER_STATE</b> enumeration to report the power state of the host controller after receiving a USBUSER_GET_POWER_STATE_MAP request. For more information about this request, see <a href="https://msdn.microsoft.com/6aba5cf4-a9fa-4d10-a212-acc79e00fa9b">IOCTL_USB_USER_REQUEST</a>.




## -see-also




<a href="https://msdn.microsoft.com/6aba5cf4-a9fa-4d10-a212-acc79e00fa9b">IOCTL_USB_USER_REQUEST</a>



<a href="https://msdn.microsoft.com/ec09faaa-d2d3-459c-9ff2-083f0fdbbadf">USB Constants and Enumerations</a>
 

 

