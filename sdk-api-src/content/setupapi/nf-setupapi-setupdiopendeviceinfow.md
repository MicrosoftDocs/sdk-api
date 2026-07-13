---
UID: NF:setupapi.SetupDiOpenDeviceInfoW
title: SetupDiOpenDeviceInfoW function (setupapi.h)
description: The SetupDiOpenDeviceInfo function adds a device information element for a device instance to a device information set, if one does not already exist in the device information set, and retrieves information that identifies the device information element for the device instance in the device information set. (Unicode)
helpviewer_keywords: ["SetupDiOpenDeviceInfo", "SetupDiOpenDeviceInfo function [Device and Driver Installation]", "SetupDiOpenDeviceInfoW", "devinst.setupdiopendeviceinfo", "di-rtns_57646ff4-705a-46ff-9c51-49880bb19f90.xml", "setupapi/SetupDiOpenDeviceInfo"]
old-location: devinst\setupdiopendeviceinfo.htm
tech.root: devinst
ms.assetid: 0c4a2d09-62b2-43ce-a202-aeb59248d9fc
ms.date: 12/05/2018
ms.keywords: SetupDiOpenDeviceInfo, SetupDiOpenDeviceInfo function [Device and Driver Installation], SetupDiOpenDeviceInfoA, SetupDiOpenDeviceInfoW, devinst.setupdiopendeviceinfo, di-rtns_57646ff4-705a-46ff-9c51-49880bb19f90.xml, setupapi/SetupDiOpenDeviceInfo
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
 - SetupDiOpenDeviceInfoW
 - setupapi/SetupDiOpenDeviceInfoW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - ext-ms-win-setupapi-devobj-l1-1-0.dll
 - ext-ms-win-setupapi-classinstallers-l1-1-2.dll
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiOpenDeviceInfo
 - SetupDiOpenDeviceInfoW
req.apiset: ext-ms-win-setupapi-classinstallers-l1-1-1 (introduced in Windows 8.1)
---

# SetupDiOpenDeviceInfoW function


## -description

The <b>SetupDiOpenDeviceInfo</b> function adds a device information element for a device instance to a device information set, if one does not already exist in the device information set, and retrieves information that identifies the device information element for the device instance in the device information set.

## -parameters

### -param DeviceInfoSet [in]

A handle to the <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> to which <b>SetupDiOpenDeviceInfo</b> adds a device information element, if one does not already exist, for the device instance that is specified by <i>DeviceInstanceId</i>.

### -param DeviceInstanceId [in]

A pointer to a NULL-terminated string that supplies the device instance identifier of a device (for example, "Root\*PNP0500\0000"). If <i>DeviceInstanceId</i> is <b>NULL</b> or references a zero-length string, <b>SetupDiOpenDeviceInfo</b> adds a device information element to the supplied device information set, if one does not already exist, for the root device in the device tree.

### -param hwndParent [in, optional]

The handle to the top-level window to use for any user interface related to installing the device.

### -param OpenFlags [in]

A variable of DWORD type that controls how the device information element is opened. The value of this parameter can be one or more of the following:





#### DIOD_CANCEL_REMOVE

If this flag is specified and the device had been marked for pending removal, the operating system cancels the pending removal.



#### DIOD_INHERIT_CLASSDRVS

If this flag is specified, the resulting device information element inherits the class driver list, if any, associated with the device information set. In addition, if there is a selected driver for the device information set, that same driver is selected for the new device information element.

If the device information element was already present, its class driver list, if any, is replaced with the inherited list.

### -param DeviceInfoData [out, optional]

A pointer to a caller-supplied <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that receives information about the device information element for the device instance that is specified by <i>DeviceInstanceId</i>. The caller must set <b>cbSize</b> to <b>sizeof(</b>SP_DEVINFO_DATA<b>)</b>. This parameter is optional and can be <b>NULL</b>. 


##### - OpenFlags.DIOD_CANCEL_REMOVE

If this flag is specified and the device had been marked for pending removal, the operating system cancels the pending removal.


##### - OpenFlags.DIOD_INHERIT_CLASSDRVS

If this flag is specified, the resulting device information element inherits the class driver list, if any, associated with the device information set. In addition, if there is a selected driver for the device information set, that same driver is selected for the new device information element.

If the device information element was already present, its class driver list, if any, is replaced with the inherited list.

## -returns

<b>SetupDiOpenDeviceInfo</b> returns <b>TRUE</b> if it is successful. Otherwise, the function returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If this device instance is being added to a set that has an associated class, the device class must be the same or the call will fail. In this case, a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_CLASS_MISMATCH.

If the new device information element is successfully opened but the caller-supplied <i>DeviceInfoData</i> buffer is invalid, this function returns <b>FALSE</b>. In this case, a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INVALID_USER_BUFFER. However, the device information element is added as a new member of the set anyway.





> [!NOTE]
> The setupapi.h header defines SetupDiOpenDeviceInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedeviceinfoa">SetupDiCreateDeviceInfo</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdideletedeviceinfo">SetupDiDeleteDeviceInfo</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdeviceinfo">SetupDiEnumDeviceInfo</a>
