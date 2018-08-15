---
UID: NS:setupapi._SP_DEVICE_INTERFACE_DATA
title: "_SP_DEVICE_INTERFACE_DATA"
author: windows-sdk-content
description: An SP_DEVICE_INTERFACE_DATA structure defines a device interface in a device information set.
old-location: devinst\sp_device_interface_data.htm
old-project: devinst
ms.assetid: df142e95-aa1c-4d3e-90c6-bac86effbd5d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PSP_DEVICE_INTERFACE_DATA, PSP_DEVICE_INTERFACE_DATA, PSP_DEVICE_INTERFACE_DATA structure pointer [Device and Driver Installation], SP_DEVICE_INTERFACE_DATA, SP_DEVICE_INTERFACE_DATA structure [Device and Driver Installation], SP_INTERFACE_DEVICE_DATA, _SP_DEVICE_INTERFACE_DATA, devinst.sp_device_interface_data, di-struct_6ad1a986-b29c-4adc-af28-e8895eee5ac4.xml, setupapi/PSP_DEVICE_INTERFACE_DATA, setupapi/SP_DEVICE_INTERFACE_DATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: setupapi.h
req.include-header: Setupapi.h
req.redist: 
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
tech.root: 
req.typenames: SP_DEVICE_INTERFACE_DATA, *PSP_DEVICE_INTERFACE_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - setupapi.h
api_name:
 - SP_DEVICE_INTERFACE_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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




<a href="https://msdn.microsoft.com/9dd44297-6e51-425d-a355-f2ea78757bf7">SP_DEVICE_INTERFACE_DETAIL_DATA</a>



<a href="https://msdn.microsoft.com/e5f78c34-b61c-4fcb-b021-fb8d07c2d841">SetupDiCreateDeviceInterface</a>



<a href="https://msdn.microsoft.com/5095404d-2447-407e-99e2-dd3ef3c3b905">SetupDiEnumDeviceInterfaces</a>



<a href="https://msdn.microsoft.com/eb36da2a-4ff1-4f2b-abc6-9bdaf491252f">SetupDiGetDeviceInterfaceAlias</a>



<a href="https://msdn.microsoft.com/31ce43e5-08b4-4c1d-b31f-77ee4e278927">SetupDiOpenDeviceInterface</a>



<a href="https://msdn.microsoft.com/1be4dd1e-6bef-4ef6-9db3-6725c27ec16d">SetupDiSetDeviceInterfaceDefault</a>
 

 

