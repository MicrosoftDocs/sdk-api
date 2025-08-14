---
UID: NF:setupapi.SetupDiSetClassInstallParamsW
title: SetupDiSetClassInstallParamsW function (setupapi.h)
description: The SetupDiSetClassInstallParams function sets or clears class install parameters for a device information set or a particular device information element. (Unicode)
helpviewer_keywords: ["SetupDiSetClassInstallParams", "SetupDiSetClassInstallParams function [Device and Driver Installation]", "SetupDiSetClassInstallParamsW", "devinst.setupdisetclassinstallparams", "di-rtns_4bbd92e2-cdae-4b03-9b30-931b6155dc2c.xml", "setupapi/SetupDiSetClassInstallParams"]
old-location: devinst\setupdisetclassinstallparams.htm
tech.root: devinst
ms.assetid: a7f35e32-eaad-440b-8109-7320048ec7ba
ms.date: 12/05/2018
ms.keywords: SetupDiSetClassInstallParams, SetupDiSetClassInstallParams function [Device and Driver Installation], SetupDiSetClassInstallParamsA, SetupDiSetClassInstallParamsW, devinst.setupdisetclassinstallparams, di-rtns_4bbd92e2-cdae-4b03-9b30-931b6155dc2c.xml, setupapi/SetupDiSetClassInstallParams
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
 - SetupDiSetClassInstallParamsW
 - setupapi/SetupDiSetClassInstallParamsW
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
 - SetupDiSetClassInstallParams
 - SetupDiSetClassInstallParamsW
req.apiset: ext-ms-win-setupapi-classinstallers-l1-1-0 (introduced in Windows 8)
---

# SetupDiSetClassInstallParamsW function


## -description

The <b>SetupDiSetClassInstallParams</b> function sets or clears class install parameters for a device information set or a particular device information element.

## -parameters

### -param DeviceInfoSet [in]

A handle to the <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> for which to set class install parameters.

### -param DeviceInfoData [in, optional]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that represents the device for which to set class install parameters. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, <b>SetupDiSetClassInstallParams</b> sets the class installation parameters for the specified device. If this parameter is <b>NULL</b>, <b>SetupDiSetClassInstallParams</b> sets the class install parameters that are associated with <i>DeviceInfoSet</i>.

### -param ClassInstallParams [in, optional]

A pointer to a buffer that contains the new class install parameters to use. The <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_classinstall_header">SP_CLASSINSTALL_HEADER</a> structure at the beginning of this buffer must have its <b>cbSize</b> field set to <b>sizeof(</b>SP_CLASSINSTALL_HEADER<b>)</b> and the <b>InstallFunction</b> field must be set to the DI_FUNCTION code that reflects the type of parameters contained in the rest of the buffer. 

If <i>ClassInstallParams</i> is not specified, the current class install parameters, if any, are cleared for the specified device information set or element.

### -param ClassInstallParamsSize [in]

The size, in bytes, of the <i>ClassInstallParams</i> buffer. If the buffer is not supplied (that is, the class install parameters are being cleared), <i>ClassInstallParamsSize</i> must be 0<i>.</i>

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All parameters are validated before any changes are made. Therefore, a return value of <b>FALSE</b> indicates that no parameters were modified.

A side effect of setting class install parameters is that the DI_CLASSINSTALLPARAMS flag is set. If the caller wants to set the parameters, but disable their use, this flag must be cleared by a call to <b>SetupDiSetDeviceInstallParams</b>. 

If the class install parameters are cleared, the DI_CLASSINSTALLPARAMS flag is reset.





> [!NOTE]
> The setupapi.h header defines SetupDiSetClassInstallParams as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassinstallparamsa">SetupDiGetClassInstallParams</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetdeviceinstallparamsa">SetupDiSetDeviceInstallParams</a>
