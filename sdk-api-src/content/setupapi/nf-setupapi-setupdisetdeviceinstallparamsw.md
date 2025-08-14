---
UID: NF:setupapi.SetupDiSetDeviceInstallParamsW
title: SetupDiSetDeviceInstallParamsW function (setupapi.h)
description: The SetupDiSetDeviceInstallParams function sets device installation parameters for a device information set or a particular device information element. (Unicode)
helpviewer_keywords: ["SetupDiSetDeviceInstallParams", "SetupDiSetDeviceInstallParams function [Device and Driver Installation]", "SetupDiSetDeviceInstallParamsW", "devinst.setupdisetdeviceinstallparams", "di-rtns_4d977738-ea9e-4bb7-b0a6-37099647b8c8.xml", "setupapi/SetupDiSetDeviceInstallParams"]
old-location: devinst\setupdisetdeviceinstallparams.htm
tech.root: devinst
ms.assetid: 20384538-e124-41f7-94a6-c0fb9f5fe6a0
ms.date: 12/05/2018
ms.keywords: SetupDiSetDeviceInstallParams, SetupDiSetDeviceInstallParams function [Device and Driver Installation], SetupDiSetDeviceInstallParamsA, SetupDiSetDeviceInstallParamsW, devinst.setupdisetdeviceinstallparams, di-rtns_4d977738-ea9e-4bb7-b0a6-37099647b8c8.xml, setupapi/SetupDiSetDeviceInstallParams
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
 - SetupDiSetDeviceInstallParamsW
 - setupapi/SetupDiSetDeviceInstallParamsW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - ext-ms-win-setupapi-classinstallers-l1-1-2.dll
 - ext-ms-win-setupapi-classinstallers-l1-1-1.dll
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiSetDeviceInstallParams - SetupDiSetDeviceInstallParamsW
---

# SetupDiSetDeviceInstallParamsW function


## -description

The <b>SetupDiSetDeviceInstallParams</b> function sets device installation parameters for a device information set or a particular device information element.

## -parameters

### -param DeviceInfoSet [in]

A handle to the <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> for which to set device installation parameters.

### -param DeviceInfoData [in, optional]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that specifies a device information element in <i>DeviceInfoSet</i>. This parameter is optional and can be set to <b>NULL</b>. If this parameter is specified, <b>SetupDiSetDeviceInstallParams</b> sets the installation parameters for the specified device. If this parameter is <b>NULL</b>, <b>SetupDiSetDeviceInstallParams</b> sets the installation parameters that are associated with the global class driver list for <i>DeviceInfoSet</i>.

### -param DeviceInstallParams [in]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinstall_params_a">SP_DEVINSTALL_PARAMS</a> structure that contains the new values of the parameters. The <i>DeviceInstallParams.</i><b>cbSize</b> must be set to the size, in bytes, of the structure before this function is called.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All parameters are validated before any changes are made. Therefore, a return value of <b>FALSE</b> indicates that no parameters were modified.





> [!NOTE]
> The setupapi.h header defines SetupDiSetDeviceInstallParams as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceinstallparamsa">SetupDiGetDeviceInstallParams</a>
