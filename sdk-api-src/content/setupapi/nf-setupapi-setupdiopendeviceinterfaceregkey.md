---
UID: NF:setupapi.SetupDiOpenDeviceInterfaceRegKey
title: SetupDiOpenDeviceInterfaceRegKey function (setupapi.h)
description: The SetupDiOpenDeviceInterfaceRegKey function opens the registry subkey that is used by applications and drivers to store information that is specific to a device interface.
helpviewer_keywords: ["SetupDiOpenDeviceInterfaceRegKey","SetupDiOpenDeviceInterfaceRegKey function [Device and Driver Installation]","devinst.setupdiopendeviceinterfaceregkey","di-rtns_420dfbe9-7cb3-4ecb-9341-b40fbc76a50e.xml","setupapi/SetupDiOpenDeviceInterfaceRegKey"]
old-location: devinst\setupdiopendeviceinterfaceregkey.htm
tech.root: devinst
ms.assetid: 950dddcb-2a59-4c2d-826b-147e9acf401a
ms.date: 12/05/2018
ms.keywords: SetupDiOpenDeviceInterfaceRegKey, SetupDiOpenDeviceInterfaceRegKey function [Device and Driver Installation], devinst.setupdiopendeviceinterfaceregkey, di-rtns_420dfbe9-7cb3-4ecb-9341-b40fbc76a50e.xml, setupapi/SetupDiOpenDeviceInterfaceRegKey
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: DesktopFor universal, call CM_Open_Device_Interface_Key
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
 - SetupDiOpenDeviceInterfaceRegKey
 - setupapi/SetupDiOpenDeviceInterfaceRegKey
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
 - SetupDiOpenDeviceInterfaceRegKey
---

# SetupDiOpenDeviceInterfaceRegKey function


## -description

The <b>SetupDiOpenDeviceInterfaceRegKey</b> function opens the registry subkey that is used by applications and drivers to store information that is specific to a device interface.

## -parameters

### -param DeviceInfoSet [in]

A pointer to a <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains the device interface for which to open a registry subkey.

### -param DeviceInterfaceData [in]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_device_interface_data">SP_DEVICE_INTERFACE_DATA</a> structure that specifies the device interface. This pointer can be returned by <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedeviceinterfacea">SetupDiCreateDeviceInterface</a> or <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces">SetupDiEnumDeviceInterfaces</a>.

### -param Reserved

Reserved. Must be zero.

### -param samDesired [in]

The requested registry security access to the registry subkey. For information about registry security access values of type REGSAM, see the Microsoft Windows SDK documentation.

## -returns

<b>SetupDiOpenDeviceInterfaceRegKey</b> returns a handle to the opened registry key. If the function fails, it returns INVALID_HANDLE_VALUE. To get extended error information, call <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Depending on the value that is passed in the <i>samDesired</i> parameter, it might be necessary for the caller of this function to be a member of the Administrators group.

Close the handle returned from by function by calling <a href="/windows/win32/api/winreg/nf-winreg-regclosekey">RegCloseKey</a>.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedeviceinterfacea">SetupDiCreateDeviceInterface</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedeviceinterfaceregkeya">SetupDiCreateDeviceInterfaceRegKey</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces">SetupDiEnumDeviceInterfaces</a>