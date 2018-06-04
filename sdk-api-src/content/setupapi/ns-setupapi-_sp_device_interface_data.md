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

# _SP_DEVICE_INTERFACE_DATA structure


## -description


An SP_DEVICE_INTERFACE_DATA structure defines a device interface in a device information set.


## -struct-fields




### -field cbSize

The size, in bytes, of the SP_DEVICE_INTERFACE_DATA structure. For more information, see the Remarks section. 


### -field InterfaceClassGuid

The GUID for the class to which the device interface belongs.


### -field Flags

Can be one or more of the following:





#### SPINT_ACTIVE

The interface is active (enabled).



#### SPINT_DEFAULT

The interface is the default interface for the device class.



#### SPINT_REMOVED

The interface is removed.


### -field Reserved

Reserved. Do not use.


## -remarks



A SetupAPI function that takes an instance of the SP_DEVICE_INTERFACE_DATA structure as a parameter verifies whether the <b>cbSize</b> member of the supplied structure is equal to the size, in bytes, of the structure. If the <b>cbSize</b> member is not set correctly, the function will fail and set an error code of ERROR_INVALID_USER_BUFFER.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552343">SP_DEVICE_INTERFACE_DETAIL_DATA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550965">SetupDiCreateDeviceInterface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551015">SetupDiEnumDeviceInterfaces</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551108">SetupDiGetDeviceInterfaceAlias</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552074">SetupDiOpenDeviceInterface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552149">SetupDiSetDeviceInterfaceDefault</a>
 

 

