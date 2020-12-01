---
UID: NS:setupapi._SP_DEVICE_INTERFACE_DATA
title: SP_DEVICE_INTERFACE_DATA (setupapi.h)
description: An SP_DEVICE_INTERFACE_DATA structure defines a device interface in a device information set.
helpviewer_keywords: ["*PSP_DEVICE_INTERFACE_DATA","PSP_DEVICE_INTERFACE_DATA","PSP_DEVICE_INTERFACE_DATA structure pointer [Device and Driver Installation]","SP_DEVICE_INTERFACE_DATA","SP_DEVICE_INTERFACE_DATA structure [Device and Driver Installation]","SP_INTERFACE_DEVICE_DATA","devinst.sp_device_interface_data","di-struct_6ad1a986-b29c-4adc-af28-e8895eee5ac4.xml","setupapi/PSP_DEVICE_INTERFACE_DATA","setupapi/SP_DEVICE_INTERFACE_DATA"]
old-location: devinst\sp_device_interface_data.htm
tech.root: devinst
ms.assetid: df142e95-aa1c-4d3e-90c6-bac86effbd5d
ms.date: 12/05/2018
ms.keywords: '*PSP_DEVICE_INTERFACE_DATA, PSP_DEVICE_INTERFACE_DATA, PSP_DEVICE_INTERFACE_DATA structure pointer [Device and Driver Installation], SP_DEVICE_INTERFACE_DATA, SP_DEVICE_INTERFACE_DATA structure [Device and Driver Installation], SP_INTERFACE_DEVICE_DATA, devinst.sp_device_interface_data, di-struct_6ad1a986-b29c-4adc-af28-e8895eee5ac4.xml, setupapi/PSP_DEVICE_INTERFACE_DATA, setupapi/SP_DEVICE_INTERFACE_DATA'
req.header: setupapi.h
req.include-header: Setupapi.h
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
req.typenames: SP_DEVICE_INTERFACE_DATA, *PSP_DEVICE_INTERFACE_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SP_DEVICE_INTERFACE_DATA
 - setupapi/_SP_DEVICE_INTERFACE_DATA
 - PSP_DEVICE_INTERFACE_DATA
 - setupapi/PSP_DEVICE_INTERFACE_DATA
 - SP_DEVICE_INTERFACE_DATA
 - setupapi/SP_DEVICE_INTERFACE_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - setupapi.h
api_name:
 - SP_DEVICE_INTERFACE_DATA
---

# SP_DEVICE_INTERFACE_DATA structure


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

<a href="/windows/win32/api/setupapi/ns-setupapi-sp_device_interface_detail_data_a">SP_DEVICE_INTERFACE_DETAIL_DATA</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedeviceinterfacea">SetupDiCreateDeviceInterface</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces">SetupDiEnumDeviceInterfaces</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceinterfacealias">SetupDiGetDeviceInterfaceAlias</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea">SetupDiOpenDeviceInterface</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetdeviceinterfacedefault">SetupDiSetDeviceInterfaceDefault</a>