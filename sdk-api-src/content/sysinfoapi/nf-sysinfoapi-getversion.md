---
UID: NF:sysinfoapi.GetVersion
title: GetVersion function (sysinfoapi.h)
description: With the release of Windows 8.1, the behavior of the GetVersion API has changed in the value it will return for the operating system version. The value returned by the GetVersion function now depends on how the application is manifested.
helpviewer_keywords: ["GetVersion","GetVersion function","_win32_getversion","base.getversion","sysinfoapi/GetVersion"]
old-location: base\getversion.htm
tech.root: winprog
ms.assetid: 25cb87c6-e4a5-447e-8153-f12638859d00
ms.date: 12/05/2018
ms.keywords: GetVersion, GetVersion function, _win32_getversion, base.getversion, sysinfoapi/GetVersion
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - GetVersion
 - sysinfoapi/GetVersion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-sysinfo-l1-2-7.dll
 - api-ms-win-core-sysinfo-l1-2-6.dll
 - api-ms-win-core-sysinfo-l1-2-5.dll
 - api-ms-win-core-sysinfo-l1-2-4.dll
 - Kernel32.dll
 - API-MS-Win-Core-SysInfo-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-0.dll
 - API-MS-Win-Core-SysInfo-l1-2-1.dll
 - API-MS-Win-Core-SysInfo-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-3.dll
api_name:
 - GetVersion
---

# GetVersion function


## -description

<b>GetVersion</b> may be altered or unavailable for releases after Windows 8.1. Instead, use the <a href="/windows/desktop/SysInfo/version-helper-apis">Version Helper functions</a>. For Windows 10 apps, please see [Targeting your applications for Windows](/windows/win32/sysinfo/targeting-your-application-at-windows-8-1).

With the release of Windows 8.1, the behavior of the <b>GetVersion</b> API has changed in the value it will return for the operating system version. The value returned by the <b>GetVersion</b> function now depends on how the application is manifested. 

Applications not manifested for Windows 8.1 or Windows 10 will return the Windows 8 OS version value (6.2).  Once an application is manifested for a given operating system version, <b>GetVersion</b> will always return the version that the application is manifested for in future releases.  To manifest your applications for Windows 8.1 or Windows 10, refer to <a href="/windows/desktop/SysInfo/targeting-your-application-at-windows-8-1">Targeting your application for Windows</a>.



## -returns

If the function succeeds, the return value includes the major and minor version numbers of the operating system in the low-order word, and information about the operating system platform in the high-order word.

For all platforms, the low-order word contains the version number of the operating system. The low-order byte of this word specifies the major version number, in hexadecimal notation. The high-order byte specifies the minor version (revision) number, in hexadecimal notation. The  high-order bit is zero, the next 7 bits represent the build number, and the low-order byte is 5.

## -remarks

The 
<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversionexa">GetVersionEx</a> function was developed because many existing applications err when examining the packed <b>DWORD</b> value returned by 
<b>GetVersion</b>, transposing the major and minor version numbers. 
<b>GetVersionEx</b> forces applications to explicitly examine each element of version information. 
<a href="/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa">VerifyVersionInfo</a> eliminates further potential for error by comparing the required system version with the current system version for you.


#### Examples

The following code fragment illustrates how to extract information from the 
<b>GetVersion</b> return value: <a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">OSVERSIONINFOEX</a>



```cpp
#include <windows.h>
#include <stdio.h>

void main()
{
    DWORD dwVersion = 0; 
    DWORD dwMajorVersion = 0;
    DWORD dwMinorVersion = 0; 
    DWORD dwBuild = 0;

    dwVersion = GetVersion();
 
    // Get the Windows version.

    dwMajorVersion = (DWORD)(LOBYTE(LOWORD(dwVersion)));
    dwMinorVersion = (DWORD)(HIBYTE(LOWORD(dwVersion)));

    // Get the build number.

    if (dwVersion < 0x80000000)              
        dwBuild = (DWORD)(HIWORD(dwVersion));

    printf("Version is %d.%d (%d)\n", 
                dwMajorVersion,
                dwMinorVersion,
                dwBuild);
}

```

## -see-also

- <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversionexa">GetVersionEx</a>
- <a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoa">OSVERSIONINFO</a>
- <a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">OSVERSIONINFOEX</a>
- <a href="/windows/desktop/SysInfo/operating-system-version">Operating System Version</a>
- <a href="/windows/desktop/SysInfo/system-information-functions">System Information Functions</a>
- <a href="/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa">VerifyVersionInfo</a>
- <a href="/windows/desktop/SysInfo/version-helper-apis">Version Helper functions</a>
