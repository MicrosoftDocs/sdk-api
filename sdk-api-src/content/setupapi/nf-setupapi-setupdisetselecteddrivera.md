---
UID: NF:setupapi.SetupDiSetSelectedDriverA
title: SetupDiSetSelectedDriverA function (setupapi.h)
description: The SetupDiSetSelectedDriver function sets, or resets, the selected driver for a device information element or the selected class driver for a device information set. (ANSI)
helpviewer_keywords: ["SetupDiSetSelectedDriverA", "di-rtns_823d52e2-7c55-4c52-bccc-809135f28251.xml"]
old-location: devinst\setupdisetselecteddriver.htm
tech.root: devinst
ms.assetid: 791df876-9037-405b-b899-eea2b577d923
ms.date: 12/05/2018
ms.keywords: SetupDiSetSelectedDriver, SetupDiSetSelectedDriver function [Device and Driver Installation], SetupDiSetSelectedDriverA, SetupDiSetSelectedDriverW, devinst.setupdisetselecteddriver, di-rtns_823d52e2-7c55-4c52-bccc-809135f28251.xml, setupapi/SetupDiSetSelectedDriver
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
 - SetupDiSetSelectedDriverA
 - setupapi/SetupDiSetSelectedDriverA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiSetSelectedDriver - SetupDiSetSelectedDriverA
---

# SetupDiSetSelectedDriverA function


## -description

The <b>SetupDiSetSelectedDriver</b> function sets, or resets, the selected driver for a device information element or the selected class driver for a device information set.

## -parameters

### -param DeviceInfoSet [in]

A handle to the <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains the driver list from which to select a driver for a device information element or for the device information set.

### -param DeviceInfoData [in, out]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, <b>SetupDiSetSelectedDriver</b> sets, or resets, the selected driver for the specified device. If this parameter is <b>NULL</b>, <b>SetupDiSetSelectedDriver</b> sets, or resets, the selected class driver for <i>DeviceInfoSet</i>.

### -param DriverInfoData [in, out]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_drvinfo_data_v1_a">SP_DRVINFO_DATA</a> structure that specifies the driver to be selected. This parameter is optional and can be <b>NULL</b>. If this parameter and <i>DeviceInfoData</i> are supplied, the specified driver must be a member of a driver list that is associated with <i>DeviceInfoData</i>. If this parameter is specified and <i>DeviceInfoData</i> is <b>NULL</b>, the driver must be a member of the global class driver list for <i>DeviceInfoSet</i>. If this parameter is <b>NULL</b>, the selected driver is reset for the device information element, if <i>DeviceInfoData</i> is specified, or the device information set, if <i>DeviceInfoData</i> is <b>NULL</b>.

If the <i>DriverInfoData.</i><b>Reserved</b> is <b>NULL</b>, the caller is requesting a search for a driver node with the specified parameters (<b>DriverType</b>, <b>Description</b>, and <b>ProviderName</b>). If a match is found, that driver node is selected. The <b>Reserved</b> field is updated on output to reflect the actual driver node where the match was found. If a match is not found, the function fails and a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INVALID_PARAMETER.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the caller of <b>SetupDiSetSelectedDriver</b> is a member of the Administrators group, the class of the device is set to the class of the selected driver, provided that the two classes are different.

If <i>DriverInfoData</i> is <b>NULL</b>, <b>SetupDiSetSelectedDriver</b> resets the selected driver. As a result, there is no selected driver. 





> [!NOTE]
> The setupapi.h header defines SetupDiSetSelectedDriver as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetselecteddrivera">SetupDiGetSelectedDriver</a>
