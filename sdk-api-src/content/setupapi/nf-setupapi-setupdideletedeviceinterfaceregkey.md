---
UID: NF:setupapi.SetupDiDeleteDeviceInterfaceRegKey
title: SetupDiDeleteDeviceInterfaceRegKey function (setupapi.h)
description: The SetupDiDeleteDeviceInterfaceRegKey function deletes the registry subkey that is used by applications and drivers to store interface-specific information.
helpviewer_keywords: ["SetupDiDeleteDeviceInterfaceRegKey","SetupDiDeleteDeviceInterfaceRegKey function [Device and Driver Installation]","devinst.setupdideletedeviceinterfaceregkey","di-rtns_73c5871c-1386-4362-be95-e4e49a052cf5.xml","setupapi/SetupDiDeleteDeviceInterfaceRegKey"]
old-location: devinst\setupdideletedeviceinterfaceregkey.htm
tech.root: devinst
ms.assetid: 470c96d4-b04f-4c9f-9ce3-9ba3d9ae49c1
ms.date: 12/05/2018
ms.keywords: SetupDiDeleteDeviceInterfaceRegKey, SetupDiDeleteDeviceInterfaceRegKey function [Device and Driver Installation], devinst.setupdideletedeviceinterfaceregkey, di-rtns_73c5871c-1386-4362-be95-e4e49a052cf5.xml, setupapi/SetupDiDeleteDeviceInterfaceRegKey
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
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
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupDiDeleteDeviceInterfaceRegKey
 - setupapi/SetupDiDeleteDeviceInterfaceRegKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-setupapi-devobj-l1-1-0.dll
 - Setupapi.dll
api_name:
 - SetupDiDeleteDeviceInterfaceRegKey
---

# SetupDiDeleteDeviceInterfaceRegKey function


## -description

The <b>SetupDiDeleteDeviceInterfaceRegKey</b> function deletes the registry subkey that is used by applications and drivers to store interface-specific information.

## -parameters

### -param DeviceInfoSet [in]

A pointer to a <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains the interface for which to delete interface-specific information in the registry. The device information set must not contain remote elements.

### -param DeviceInterfaceData [in]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_device_interface_data">SP_DEVICE_INTERFACE_DATA</a> structure that specifies the device interface in <i>DeviceInfoSet</i>. This pointer is possibly returned by <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedeviceinterfacea">SetupDiCreateDeviceInterface</a> or <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces">SetupDiEnumDeviceInterfaces</a>.

### -param Reserved

Reserved. Must be zero.

## -returns

<b>SetupDiDeleteDeviceInterfaceRegKey</b> returns <b>TRUE</b> if it is successful; otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The caller of this function must be a member of the Administrators group.

<b>SetupDiDeleteDeviceInterfaceRegKey</b> deletes the subkey used by drivers and applications to store information about the device interface instance. This subkey was created by <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedeviceinterfaceregkeya">SetupDiCreateDeviceInterfaceRegKey</a> or by the driver's call to an associated <a href="/windows-hardware/drivers/ddi/_kernel/#io-manager-routines">I/O manager routine</a>. <b>SetupDiDeleteDeviceInterfaceRegKey</b> does not affect the main registry key for the device interface instance nor any other subkeys that may have been created.

The <i>DeviceInfoSet</i> must only contain elements on the local computer.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedeviceinterfacea">SetupDiCreateDeviceInterface</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedeviceinterfaceregkeya">SetupDiCreateDeviceInterfaceRegKey</a>