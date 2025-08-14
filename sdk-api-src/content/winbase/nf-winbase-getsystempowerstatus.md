---
UID: NF:winbase.GetSystemPowerStatus
title: GetSystemPowerStatus function (winbase.h)
description: Retrieves the power status of the system. The status indicates whether the system is running on AC or DC power, whether the battery is currently charging, how much battery life remains, and if battery saver is on or off.
helpviewer_keywords: ["GetSystemPowerStatus","GetSystemPowerStatus function","_win32_getsystempowerstatus","base.getsystempowerstatus","winbase/GetSystemPowerStatus"]
old-location: base\getsystempowerstatus.htm
tech.root: base
ms.assetid: 6d440ef2-2b9d-4f7a-a445-2420f07f3784
ms.date: 12/05/2018
ms.keywords: GetSystemPowerStatus, GetSystemPowerStatus function, _win32_getsystempowerstatus, base.getsystempowerstatus, winbase/GetSystemPowerStatus
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetSystemPowerStatus
 - winbase/GetSystemPowerStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GetSystemPowerStatus
---

# GetSystemPowerStatus function


## -description

Retrieves the power status of the system. The status indicates whether the system is running on AC or DC power, whether the battery is currently charging, how much battery life remains, and if battery saver is on or off.

## -parameters

### -param lpSystemPowerStatus [out]

A pointer to a 
<a href="/windows/desktop/api/winbase/ns-winbase-system_power_status">SYSTEM_POWER_STATUS</a> structure that receives status information.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To compile an application that uses this function, define the _WIN32_WINNT macro as 0x0400 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/Power/power-management-functions">Power Management Functions</a>



<a href="/windows/desktop/api/winbase/ns-winbase-system_power_status">SYSTEM_POWER_STATUS</a>



<a href="/windows/desktop/Power/system-power-status">System Power Status</a>