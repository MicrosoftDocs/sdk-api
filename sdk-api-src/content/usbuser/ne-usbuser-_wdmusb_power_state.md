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



The USB stack uses the <b>WDMUSB_POWER_STATE</b> enumeration to report the power state of the host controller after receiving a USBUSER_GET_POWER_STATE_MAP request. For more information about this request, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff537344">IOCTL_USB_USER_REQUEST</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539322">USB Constants and Enumerations</a>
 

 

