---
UID: NF:setupapi.SetupDiCreateDeviceInterfaceRegKeyW
title: SetupDiCreateDeviceInterfaceRegKeyW function (setupapi.h)
description: The SetupDiCreateDeviceInterfaceRegKey function creates a registry key for storing information about a device interface and returns a handle to the key. (Unicode)
helpviewer_keywords: ["SetupDiCreateDeviceInterfaceRegKey", "SetupDiCreateDeviceInterfaceRegKey function [Device and Driver Installation]", "SetupDiCreateDeviceInterfaceRegKeyW", "devinst.setupdicreatedeviceinterfaceregkey", "di-rtns_4b18b81a-e8ae-4d04-ae67-26cb21472e23.xml", "setupapi/SetupDiCreateDeviceInterfaceRegKey"]
old-location: devinst\setupdicreatedeviceinterfaceregkey.htm
tech.root: devinst
ms.assetid: 1be942a1-428d-4cc4-bc9f-9f21243c3d21
ms.date: 12/05/2018
ms.keywords: SetupDiCreateDeviceInterfaceRegKey, SetupDiCreateDeviceInterfaceRegKey function [Device and Driver Installation], SetupDiCreateDeviceInterfaceRegKeyA, SetupDiCreateDeviceInterfaceRegKeyW, devinst.setupdicreatedeviceinterfaceregkey, di-rtns_4b18b81a-e8ae-4d04-ae67-26cb21472e23.xml, setupapi/SetupDiCreateDeviceInterfaceRegKey
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupDiCreateDeviceInterfaceRegKeyW
 - setupapi/SetupDiCreateDeviceInterfaceRegKeyW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - ext-ms-win-setupapi-devobj-l1-1-0.dll
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiCreateDeviceInterfaceRegKey - SetupDiCreateDeviceInterfaceRegKeyW
---

# SetupDiCreateDeviceInterfaceRegKeyW function


## -description

The <b>SetupDiCreateDeviceInterfaceRegKey</b> function creates a registry key for storing information about a device interface and returns a handle to the key.

## -parameters

### -param DeviceInfoSet [in]

A handle to a <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains the interface for which to create a registry key. The device information set must not contain remote elements.

### -param DeviceInterfaceData [in]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_device_interface_data">SP_DEVICE_INTERFACE_DATA</a> structure that specifies the device interface in <i>DeviceInfoSet</i>. This pointer is possibly returned by <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedeviceinterfacea">SetupDiCreateDeviceInterface</a>.

### -param Reserved

Reserved. Must be zero.

### -param samDesired [in]

The registry security access that the caller requests for the key that is being created. For information about registry security access values of type REGSAM, see the Microsoft Windows SDK documentation.

### -param InfHandle [in, optional]

The handle to an open INF file that contains a <i>DDInstall</i> section to be executed for the newly-created key. This parameter is optional and can be <b>NULL</b>. If this parameter is not <b>NULL</b>, <i>InfSectionName</i> must be specified as well.

### -param InfSectionName [in, optional]

A pointer to the name of an INF <i>DDInstall</i> section in the INF file that is specified by <i>InfHandle</i>. This section is executed for the newly created key. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, <i>InfHandle</i> must be specified as well.

## -returns

If <b>SetupDiCreateDeviceInterfaceRegKey</b> succeeds, the function returns a handle to the requested registry key in which interface information can be stored and retrieved. If <b>SetupDiCreateDeviceInterfaceRegKey</b> fails, the function returns INVALID_HANDLE_VALUE. Call <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to get extended error information.

## -remarks

The caller of this function must be a member of the Administrators group.

If the requested key for the device interface already exists, <b>SetupDiCreateDeviceInterfaceRegKey</b> returns a handle to that key; otherwise, <b>SetupDiCreateDeviceInterfaceRegKey</b> creates a new nonvolatile registry key for the specified device interface. Callers of this function can store private configuration data for the device interface in this key. The driver for the device can access this key using <b>Io</b><i>Xxx</i> routines.

Close the handle returned from this function by calling <a href="/windows/win32/api/winreg/nf-winreg-regclosekey">RegCloseKey</a>.

For installations that use layout files (specified by the <b>LayoutFile</b> entry in an <a href="/windows-hardware/drivers/install/inf-version-section">INF Version section</a>), the layout file must be opened by a call to <b>SetupOpenAppendInfFile</b> (described in Windows SDK documentation) before <b>SetupDiCreateDeviceInterfaceRegKey</b> is called.

The device information set specified by <i>DeviceInfoSet</i> must only contain elements on the local computer.





> [!NOTE]
> The setupapi.h header defines SetupDiCreateDeviceInterfaceRegKey as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedeviceinterfacea">SetupDiCreateDeviceInterface</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdideletedeviceinterfaceregkey">SetupDiDeleteDeviceInterfaceRegKey</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiopendeviceinterfaceregkey">SetupDiOpenDeviceInterfaceRegKey</a>
