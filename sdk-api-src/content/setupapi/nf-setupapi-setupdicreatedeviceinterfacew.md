---
UID: NF:setupapi.SetupDiCreateDeviceInterfaceW
title: SetupDiCreateDeviceInterfaceW function (setupapi.h)
description: The SetupDiCreateDeviceInterface function registers a device interface on a local system or a remote system. (Unicode)
helpviewer_keywords: ["SetupDiCreateDeviceInterface", "SetupDiCreateDeviceInterface function [Device and Driver Installation]", "SetupDiCreateDeviceInterfaceW", "devinst.setupdicreatedeviceinterface", "di-rtns_252e73f4-f140-44bf-bd81-abb08a036df7.xml", "setupapi/SetupDiCreateDeviceInterface"]
old-location: devinst\setupdicreatedeviceinterface.htm
tech.root: devinst
ms.assetid: e5f78c34-b61c-4fcb-b021-fb8d07c2d841
ms.date: 12/05/2018
ms.keywords: SetupDiCreateDeviceInterface, SetupDiCreateDeviceInterface function [Device and Driver Installation], SetupDiCreateDeviceInterfaceA, SetupDiCreateDeviceInterfaceW, devinst.setupdicreatedeviceinterface, di-rtns_252e73f4-f140-44bf-bd81-abb08a036df7.xml, setupapi/SetupDiCreateDeviceInterface
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
 - SetupDiCreateDeviceInterfaceW
 - setupapi/SetupDiCreateDeviceInterfaceW
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
 - SetupDiCreateDeviceInterface - SetupDiCreateDeviceInterfaceW
---

# SetupDiCreateDeviceInterfaceW function


## -description

The <b>SetupDiCreateDeviceInterface</b> function registers a device interface on a local system or a remote system.

## -parameters

### -param DeviceInfoSet [in]

A handle to a <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a>. This set contains a device information element that represents the device for which to register an interface. This handle is typically returned by <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassdevsw">SetupDiGetClassDevs</a>.

### -param DeviceInfoData [in]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>.

### -param InterfaceClassGuid [in]

A pointer to a class GUID that specifies the interface class for the new interface.

### -param ReferenceString [in, optional]

A pointer to a NULL-terminated string that supplies a reference string. This pointer is optional and can be <b>NULL</b>. Reference strings are used only by a few bus drivers that use device interfaces as placeholders for software devices that are created on demand.

### -param CreationFlags [in]

Reserved. Must be zero.

### -param DeviceInterfaceData [out, optional]

A pointer to a caller-initialized <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_device_interface_data">SP_DEVICE_INTERFACE_DATA</a> structure to receive information about the new device interface. This pointer is optional and can be <b>NULL</b>. If the structure is supplied, the caller must set the <b>cbSize</b> member of this structure to <b>sizeof(</b>SP_DEVICE_INTERFACE_DATA<b>)</b> before calling this function. For more information, see the following <b>Remarks</b> section.

## -returns

<b>SetupDiCreateDeviceInterface</b> returns <b>TRUE</b> if the function completed without error. If the function completed with an error, it returns <b>FALSE</b> and the error code for the failure can be retrieved by calling <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The caller of this function must be a member of the Administrators group.

<b>SetupDiCreateDeviceInterface</b> registers an interface for a device. If a device has more than one interface, call this function once for each interface being registered. 

If this function successfully registers an interface for the device that corresponds to the specified device information element, it also adds the interface to the interface list that is associated with the device information element in the specified device information set.

Before a registered interface can be used by applications and other system components the interface must be enabled by the driver for the device.

This function creates a registry key for the new device interface. Callers of this function can access nonvolatile storage under this key using <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiopendeviceinterfaceregkey">SetupDiOpenDeviceInterfaceRegKey</a>.

If <b>SetupDiCreateDeviceInterface</b> successfully creates a new device interface, but the caller-supplied buffer in the <i>DeviceInterfaceData</i> parameter is invalid, this function will return <b>FALSE</b> and a subsequent call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return ERROR_INVALID_USER_BUFFER. However, the function does create and register the new device interface. 





> [!NOTE]
> The setupapi.h header defines SetupDiCreateDeviceInterface as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiopendeviceinterfaceregkey">SetupDiOpenDeviceInterfaceRegKey</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiremovedeviceinterface">SetupDiRemoveDeviceInterface</a>
