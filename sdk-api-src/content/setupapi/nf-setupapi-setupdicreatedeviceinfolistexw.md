---
UID: NF:setupapi.SetupDiCreateDeviceInfoListExW
title: SetupDiCreateDeviceInfoListExW function (setupapi.h)
description: The SetupDiCreateDeviceInfoList function creates an empty device information set on a remote or a local computer and optionally associates the set with a device setup class . (Unicode)
helpviewer_keywords: ["SetupDiCreateDeviceInfoListEx", "SetupDiCreateDeviceInfoListEx function [Device and Driver Installation]", "SetupDiCreateDeviceInfoListExW", "devinst.setupdicreatedeviceinfolistex", "di-rtns_584dc470-c07f-4658-b16d-53a2594dabf9.xml", "setupapi/SetupDiCreateDeviceInfoListEx"]
old-location: devinst\setupdicreatedeviceinfolistex.htm
tech.root: devinst
ms.assetid: 4dae7b07-2e24-4fd8-82f2-f947296ce3c4
ms.date: 01/30/2023
ms.keywords: SetupDiCreateDeviceInfoListEx, SetupDiCreateDeviceInfoListEx function [Device and Driver Installation], SetupDiCreateDeviceInfoListExA, SetupDiCreateDeviceInfoListExW, devinst.setupdicreatedeviceinfolistex, di-rtns_584dc470-c07f-4658-b16d-53a2594dabf9.xml, setupapi/SetupDiCreateDeviceInfoListEx
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
 - SetupDiCreateDeviceInfoListExW
 - setupapi/SetupDiCreateDeviceInfoListExW
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
 - SetupDiCreateDeviceInfoListEx
 - SetupDiCreateDeviceInfoListExW
---

# SetupDiCreateDeviceInfoListExW function


## -description

The <b>SetupDiCreateDeviceInfoList</b> function creates an empty <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> on a remote or a local computer and optionally associates the set with a device setup class .

## -parameters

### -param ClassGuid [in, optional]

A pointer to the GUID of the device setup class to associate with the newly created device information set. If this parameter is specified, only devices of this class can be included in this device information set. If this parameter is set to <b>NULL</b>, the device information set is not associated with a specific device setup class.

### -param hwndParent [in, optional]

A handle to the top-level window to use for any user interface that is related to non-device-specific actions (such as a select-device dialog box that uses the global class driver list). This handle is optional and can be <b>NULL</b>. If a specific top-level window is not required, set <i>hwndParent</i> to <b>NULL</b>.

### -param MachineName [in, optional]

A pointer to a NULL-terminated string that contains the name of a computer on a network. If a name is specified, only devices on that computer can be created and opened in this device information set. If this parameter is set to <b>NULL</b>, the device information set is for devices on the local computer.

> [!CAUTION]
> Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.

### -param Reserved

Must be <b>NULL</b>.

## -returns

The function returns a handle to an empty device information set if it is successful. Otherwise, it returns INVALID_HANDLE_VALUE. To get extended error information, call <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The caller of this function must delete the returned device information set when it is no longer needed by calling <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist">SetupDiDestroyDeviceInfoList</a>. 

If the device information set is for devices on a remote computer (<i>MachineName</i> is not <b>NULL</b>), all subsequent operations on this set or any of its elements must use routines that support device information sets with remote elements. The <b>SetupDi</b><i>Xxx</i> routines that do not provide this support, such as <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicallclassinstaller">SetupDiCallClassInstaller</a>, have a statement to that effect in their reference page.





> [!NOTE]
> The setupapi.h header defines SetupDiCreateDeviceInfoListEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedeviceinfolist">SetupDiCreateDeviceInfoList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist">SetupDiDestroyDeviceInfoList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceinfolistdetaila">SetupDiGetDeviceInfoListDetail</a>
