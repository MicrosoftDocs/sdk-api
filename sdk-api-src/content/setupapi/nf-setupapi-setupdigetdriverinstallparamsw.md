---
UID: NF:setupapi.SetupDiGetDriverInstallParamsW
title: SetupDiGetDriverInstallParamsW function (setupapi.h)
description: The SetupDiGetDriverInstallParams function retrieves driver installation parameters for a device information set or a particular device information element. (Unicode)
helpviewer_keywords: ["SetupDiGetDriverInstallParams", "SetupDiGetDriverInstallParams function [Device and Driver Installation]", "SetupDiGetDriverInstallParamsW", "devinst.setupdigetdriverinstallparams", "di-rtns_b8e7fdca-3201-42f9-86b4-a8a97be8cb90.xml", "setupapi/SetupDiGetDriverInstallParams"]
old-location: devinst\setupdigetdriverinstallparams.htm
tech.root: devinst
ms.assetid: 7c5b0e3f-75cd-48e1-b84e-d81e4e4db7b2
ms.date: 12/05/2018
ms.keywords: SetupDiGetDriverInstallParams, SetupDiGetDriverInstallParams function [Device and Driver Installation], SetupDiGetDriverInstallParamsA, SetupDiGetDriverInstallParamsW, devinst.setupdigetdriverinstallparams, di-rtns_b8e7fdca-3201-42f9-86b4-a8a97be8cb90.xml, setupapi/SetupDiGetDriverInstallParams
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
 - SetupDiGetDriverInstallParamsW
 - setupapi/SetupDiGetDriverInstallParamsW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - ext-ms-win-setupapi-classinstallers-l1-1-2.dll
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiGetDriverInstallParams - SetupDiGetDriverInstallParamsW
---

# SetupDiGetDriverInstallParamsW function


## -description

The <b>SetupDiGetDriverInstallParams</b> function retrieves driver installation parameters for a device information set or a particular device information element.

## -parameters

### -param DeviceInfoSet [in]

A handle to a <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains a driver information element that represents the driver for which to retrieve installation parameters.

### -param DeviceInfoData [in, optional]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that contains a device information element that represents the device for which to retrieve installation parameters. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, <b>SetupDiGetDriverInstallParams</b> retrieves information about a driver that is a member of a driver list for the specified device. If this parameter is <b>NULL</b>, <b>SetupDiGetDriverInstallParams</b> retrieves information about a driver  that is a member of the global class driver list for <i>DeviceInfoSet</i>.

### -param DriverInfoData [in]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_drvinfo_data_v1_a">SP_DRVINFO_DATA</a> structure that specifies the driver information element that represents the driver for which to retrieve installation parameters. If <i>DeviceInfoData</i> is supplied, the driver must be a member of the driver list for the device that is specified by <i>DeviceInfoData</i>. Otherwise, the driver must be a member of the global class driver list for <i>DeviceInfoSet</i>.

### -param DriverInstallParams [out]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_drvinstall_params">SP_DRVINSTALL_PARAMS</a> structure to receive the installation parameters for this driver.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetdriverinstallparamsa">SetupDiSetDriverInstallParams</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupDiGetDriverInstallParams as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
