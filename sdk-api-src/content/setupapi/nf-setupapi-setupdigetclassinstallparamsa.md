---
UID: NF:setupapi.SetupDiGetClassInstallParamsA
title: SetupDiGetClassInstallParamsA function (setupapi.h)
description: The SetupDiGetClassInstallParams function retrieves class installation parameters for a device information set or a particular device information element. (ANSI)
helpviewer_keywords: ["SetupDiGetClassInstallParamsA", "di-rtns_2f7d5019-6b09-4dc0-8640-8a452d01e6da.xml"]
old-location: devinst\setupdigetclassinstallparams.htm
tech.root: devinst
ms.assetid: 4ac1eb44-c7d6-48f3-bc7f-fb547e5a985e
ms.date: 12/05/2018
ms.keywords: SetupDiGetClassInstallParams, SetupDiGetClassInstallParams function [Device and Driver Installation], SetupDiGetClassInstallParamsA, SetupDiGetClassInstallParamsW, devinst.setupdigetclassinstallparams, di-rtns_2f7d5019-6b09-4dc0-8640-8a452d01e6da.xml, setupapi/SetupDiGetClassInstallParams
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
 - SetupDiGetClassInstallParamsA
 - setupapi/SetupDiGetClassInstallParamsA
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
 - SetupDiGetClassInstallParams - SetupDiGetClassInstallParamsA
---

# SetupDiGetClassInstallParamsA function


## -description

The <b>SetupDiGetClassInstallParams</b> function retrieves class installation parameters for a device information set or a particular device information element.

## -parameters

### -param DeviceInfoSet [in]

A handle to a <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains the class install parameters to retrieve.

### -param DeviceInfoData [in, optional]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that specified a device information element in <i>DeviceInfoSet</i>. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, <b>SetupDiGetClassInstallParams</b> retrieves the class installation parameters for the specified device. If this parameter is <b>NULL</b>, <b>SetupDiGetClassInstallParams</b> retrieves the class install parameters for the global class driver list that is associated with <i>DeviceInfoSet</i>.

### -param ClassInstallParams [out, optional]

A pointer to a buffer that contains an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_classinstall_header">SP_CLASSINSTALL_HEADER</a> structure. This structure must have its <b>cbSize</b> member set to <b>sizeof(</b>SP_CLASSINSTALL_HEADER<b>)</b> on input or the buffer is considered to be invalid. On output, the <b>InstallFunction</b> member is filled with the <a href="/windows-hardware/drivers/install/handling-dif-codes">device installation function code</a> for the class installation parameters being retrieved. If the buffer is large enough, it also receives the class installation parameters structure specific to the function code. If <i>ClassInstallParams</i> is not specified, <i>ClassInstallParamsSize</i> must be 0.

### -param ClassInstallParamsSize [in]

The size, in bytes, of the <i>ClassInstallParams</i> buffer. If the buffer is supplied, it must be at least as large as <b>sizeof(</b>SP_CLASSINSTALL_HEADER<b>)</b>. If the buffer is not supplied, <i>ClassInstallParamsSize</i> must be 0<i>.</i>

### -param RequiredSize [out, optional]

A pointer to a variable of type DWORD that receives the number of bytes required to store the class install parameters. This parameter is optional and can be <b>NULL</b>.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The class install parameters are specific to a particular <a href="/windows-hardware/drivers/install/handling-dif-codes">device installation function code</a> that is stored in the <b>ClassInstallHeader</b> field located at the beginning of the <i>ClassInstallParams</i> buffer.





> [!NOTE]
> The setupapi.h header defines SetupDiGetClassInstallParams as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetclassinstallparamsa">SetupDiSetClassInstallParams</a>
