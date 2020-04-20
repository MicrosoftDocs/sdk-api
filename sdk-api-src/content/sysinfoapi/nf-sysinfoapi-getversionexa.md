---
UID: NF:sysinfoapi.GetVersionExA
title: GetVersionExA function (sysinfoapi.h)
description: With the release of Windows 8.1, the behavior of the GetVersionEx API has changed in the value it will return for the operating system version. The value returned by the GetVersionEx function now depends on how the application is manifested.helpviewer_keywords: ["GetVersionEx","GetVersionEx function","GetVersionExA","GetVersionExW","_win32_getversionex","base.getversionex","sysinfoapi/GetVersionEx","sysinfoapi/GetVersionExA","sysinfoapi/GetVersionExW"]
old-location: base\getversionex.htm
tech.root: SysInfo
ms.assetid: 8e3ab4d6-bacd-4bc5-b8f6-dd49289354de
ms.date: 12/05/2018
ms.keywords: GetVersionEx, GetVersionEx function, GetVersionExA, GetVersionExW, _win32_getversionex, base.getversionex, sysinfoapi/GetVersionEx, sysinfoapi/GetVersionExA, sysinfoapi/GetVersionExW
f1_keywords:
- sysinfoapi/GetVersionEx
dev_langs:
- c++
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetVersionExW (Unicode) and GetVersionExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
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
- GetVersionEx
- GetVersionExA
- GetVersionExW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetVersionExA function


## -description


<p class="CCE_Message">[<b>GetVersionEx</b> may be altered or unavailable for releases after Windows 8.1. Instead, use the <a href="https://docs.microsoft.com/windows/desktop/SysInfo/version-helper-apis">Version Helper functions</a>]

With the release of Windows 8.1, the behavior of the <b>GetVersionEx</b> API has changed in the value it will return for the operating system version. The value returned by the <b>GetVersionEx</b> function now depends on how the application is manifested. 

Applications not manifested for Windows 8.1 or Windows 10 will return the Windows 8 OS version value (6.2).  Once an application is manifested for a given operating system version, <b>GetVersionEx</b> will always return the version that the application is manifested for in future releases.  To manifest your applications for Windows 8.1 or Windows 10, refer to <a href="https://docs.microsoft.com/windows/desktop/SysInfo/targeting-your-application-at-windows-8-1">Targeting your application for Windows</a>.


## -parameters




### -param lpVersionInformation [in, out]

An 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-osversioninfoa">OSVERSIONINFO</a> or <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">OSVERSIONINFOEX</a> structure that receives the operating system information. 




Before calling the 
<b>GetVersionEx</b> function, set the <b>dwOSVersionInfoSize</b> member of the structure as appropriate to indicate which data structure is being passed to this function.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The function fails if you specify an invalid value for the <b>dwOSVersionInfoSize</b> member of the 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-osversioninfoa">OSVERSIONINFO</a> or 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">OSVERSIONINFOEX</a> structure.




## -remarks



Identifying the current operating system is usually not the best way to determine whether a particular operating system feature is present. This is because the operating system may have had new features added in a redistributable DLL. Rather than using 
<b>GetVersionEx</b> to determine the operating system platform or version number, test for the presence of the feature itself. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/SysInfo/operating-system-version">Operating System Version</a>.

The <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a> function provides additional information about the current operating system. 

<table>
<tr>
<th>Product</th>
<th>Setting</th>
</tr>
<tr>
<td>Windows XP Media Center Edition</td>
<td>SM_MEDIACENTER</td>
</tr>
<tr>
<td>Windows XP Starter Edition</td>
<td>SM_STARTER</td>
</tr>
<tr>
<td>Windows XP Tablet PC Edition</td>
<td>SM_TABLETPC</td>
</tr>
<tr>
<td>Windows Server 2003 R2</td>
<td>SM_SERVERR2</td>
</tr>
</table>
 

To check for specific operating systems or operating system features, use the <a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-isos">IsOS</a> function. The <a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getproductinfo">GetProductInfo</a> function retrieves the product type.

To retrieve information for the operating system on a remote computer, use the <a href="https://docs.microsoft.com/windows/desktop/api/lmwksta/nf-lmwksta-netwkstagetinfo">NetWkstaGetInfo</a> function, the <a href="https://docs.microsoft.com/windows/desktop/CIMWin32Prov/win32-operatingsystem">Win32_OperatingSystem</a> WMI class, or the <a href="https://docs.microsoft.com/windows/desktop/ADSI/iadscomputer-property-methods">OperatingSystem</a> property of the <b>IADsComputer</b> interface.

To compare the current system version to a required version, use the 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa">VerifyVersionInfo</a> function instead of using 
<b>GetVersionEx</b> to perform the comparison yourself.

If compatibility mode is in effect, the <b>GetVersionEx</b> function reports the operating system as it identifies itself, which may not be the operating system that is installed. For example, if compatibility mode is in effect, <b>GetVersionEx</b> reports the operating system that is selected for <a href="https://msdn.microsoft.com/library/bb757005.aspx">application compatibility</a>.


#### Examples

When using the 
<b>GetVersionEx</b> function to determine whether your application is running on a particular version of the operating system, check for version numbers that are greater than or equal to the desired version numbers. This ensures that the test succeeds for later versions of the operating system. For example, if your application requires Windows XP or later, use the following test.


```cpp
#include <windows.h>
#include <stdio.h>

void main()
{
    OSVERSIONINFO osvi;
    BOOL bIsWindowsXPorLater;

    ZeroMemory(&osvi, sizeof(OSVERSIONINFO));
    osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFO);

    GetVersionEx(&osvi);

    bIsWindowsXPorLater = 
       ( (osvi.dwMajorVersion > 5) ||
       ( (osvi.dwMajorVersion == 5) && (osvi.dwMinorVersion >= 1) ));

    if(bIsWindowsXPorLater)
        printf("The system meets the requirements.\n");
    else printf("The system does not meet the requirements.\n");
}

```


For an example that identifies the current operating system, see 
<a href="https://docs.microsoft.com/windows/desktop/SysInfo/getting-the-system-version">Getting the System Version</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion">GetVersion</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-osversioninfoa">OSVERSIONINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">OSVERSIONINFOEX</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/operating-system-version">Operating System Version</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/system-information-functions">System Information Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa">VerifyVersionInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/version-helper-apis">Version Helper functions</a>
 

 

