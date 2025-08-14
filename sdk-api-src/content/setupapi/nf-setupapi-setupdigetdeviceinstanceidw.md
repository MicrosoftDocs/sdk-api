---
UID: NF:setupapi.SetupDiGetDeviceInstanceIdW
title: SetupDiGetDeviceInstanceIdW function (setupapi.h)
description: The SetupDiGetDeviceInstanceId function retrieves the device instance ID that is associated with a device information element. (Unicode)
helpviewer_keywords: ["SetupDiGetDeviceInstanceId", "SetupDiGetDeviceInstanceId function [Device and Driver Installation]", "SetupDiGetDeviceInstanceIdW", "devinst.setupdigetdeviceinstanceid", "di-rtns_f7f2bb12-37a0-489f-a1e7-0ca67600876c.xml", "setupapi/SetupDiGetDeviceInstanceId"]
old-location: devinst\setupdigetdeviceinstanceid.htm
tech.root: devinst
ms.assetid: 43ad298d-2ff4-445a-aa23-1319d5f990c8
ms.date: 12/05/2018
ms.keywords: SetupDiGetDeviceInstanceId, SetupDiGetDeviceInstanceId function [Device and Driver Installation], SetupDiGetDeviceInstanceIdA, SetupDiGetDeviceInstanceIdW, devinst.setupdigetdeviceinstanceid, di-rtns_f7f2bb12-37a0-489f-a1e7-0ca67600876c.xml, setupapi/SetupDiGetDeviceInstanceId
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
 - SetupDiGetDeviceInstanceIdW
 - setupapi/SetupDiGetDeviceInstanceIdW
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
 - ext-ms-win-setupapi-classinstallers-l1-1-1.dll
 - ext-ms-win-setupapi-classinstallers-l1-1-0.dll
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiGetDeviceInstanceId - SetupDiGetDeviceInstanceIdW
---

# SetupDiGetDeviceInstanceIdW function


## -description

The <b>SetupDiGetDeviceInstanceId</b> function retrieves the <a href="/windows-hardware/drivers/install/device-instance-ids">device instance ID</a> that is associated with a device information element.

> [!NOTE]
> In Windows Vista and later versions of Windows, the [unified device property model](/windows-hardware/drivers/install/unified-device-property-model--windows-vista-and-later-) uses the [**DEVPKEY_Device_InstanceId**](/windows-hardware/drivers/install/devpkey-device-instanceid) [property key](/windows-hardware/drivers/install/property-keys) to represent the device instance identifier. See [Retrieving a Device Instance Identifier](/windows-hardware/drivers/install/retrieving-a-device-instance-identifier) for details.

## -parameters

### -param DeviceInfoSet [in]

A handle to the <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains the device information element that represents the device for which to retrieve a device instance ID.

### -param DeviceInfoData [in]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>.

### -param DeviceInstanceId [out, optional]

A pointer to the character buffer that will receive the NULL-terminated device instance ID for the specified device information element. For information about device instance IDs, see <a href="/windows-hardware/drivers/install/device-identification-strings">Device Identification Strings</a>.

### -param DeviceInstanceIdSize [in]

The size, in characters, of the <i>DeviceInstanceId</i> buffer.

### -param RequiredSize [out, optional]

A pointer to the variable that receives the number of characters required to store the device instance ID.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedevregkeya">SetupDiCreateDevRegKey</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedeviceinfoa">SetupDiCreateDeviceInfo</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiopendevregkey">SetupDiOpenDevRegKey</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiopendeviceinfoa">SetupDiOpenDeviceInfo</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupDiGetDeviceInstanceId as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
