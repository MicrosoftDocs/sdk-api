---
UID: NF:sysinfoapi.GetVersion
title: GetVersion function
author: windows-sdk-content
description: With the release of Windows 8.1, the behavior of the GetVersion API has changed in the value it will return for the operating system version. The value returned by the GetVersion function now depends on how the application is manifested.
old-location: base\getversion.htm
tech.root: SysInfo
ms.assetid: 25cb87c6-e4a5-447e-8153-f12638859d00
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetVersion, GetVersion function, _win32_getversion, base.getversion, sysinfoapi/GetVersion
ms.topic: function
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
 - GetVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetVersion function


## -description


<p class="CCE_Message">[<b>GetVersion</b> may be altered or unavailable for releases after Windows 8.1. Instead, use the <a href="https://msdn.microsoft.com/2FAF67CD-CEEA-4096-B482-F5E2DF8D6C34">Version Helper functions</a>]

With the release of Windows 8.1, the behavior of the <b>GetVersion</b> API has changed in the value it will return for the operating system version. The value returned by the <b>GetVersion</b> function now depends on how the application is manifested. 

Applications not manifested for Windows 8.1 or Windows 10 will return the Windows 8 OS version value (6.2).  Once an application is manifested for a given operating system version, <b>GetVersion</b> will always return the version that the application is manifested for in future releases.  To manifest your applications for Windows 8.1 or Windows 10, refer to <a href="https://msdn.microsoft.com/E7A1A16A-95B3-4B45-81AD-A19E33F15AE4">Targeting your application for Windows</a>.


## -parameters






## -returns



If the function succeeds, the return value includes the major and minor version numbers of the operating system in the low-order word, and information about the operating system platform in the high-order word.

For all platforms, the low-order word contains the version number of the operating system. The low-order byte of this word specifies the major version number, in hexadecimal notation. The high-order byte specifies the minor version (revision) number, in hexadecimal notation. The  high-order bit is zero, the next 7 bits represent the build number, and the low-order byte is 5.




## -remarks



The 
<a href="https://msdn.microsoft.com/8e3ab4d6-bacd-4bc5-b8f6-dd49289354de">GetVersionEx</a> function was developed because many existing applications err when examining the packed <b>DWORD</b> value returned by 
<b>GetVersion</b>, transposing the major and minor version numbers. 
<b>GetVersionEx</b> forces applications to explicitly examine each element of version information. 
<a href="https://msdn.microsoft.com/791bc6bf-f486-4110-b6ea-30a0935040b2">VerifyVersionInfo</a> eliminates further potential for error by comparing the required system version with the current system version for you.


#### Examples

The following code fragment illustrates how to extract information from the 
<b>GetVersion</b> return value: <a href="https://msdn.microsoft.com/4ab07a72-404d-459b-b061-b3b06b5db37e">OSVERSIONINFOEX</a>


<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include <windows.h>
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
</pre>
</td>
</tr>
</table></span></div>





## -see-also




<a href="https://msdn.microsoft.com/8e3ab4d6-bacd-4bc5-b8f6-dd49289354de">GetVersionEx</a>



<a href="https://msdn.microsoft.com/a173df17-dad2-4330-aa66-4ff789fd7cc2">OSVERSIONINFO</a>



<a href="https://msdn.microsoft.com/4ab07a72-404d-459b-b061-b3b06b5db37e">OSVERSIONINFOEX</a>



<a href="https://msdn.microsoft.com/1a70b1d9-ed66-4201-9921-4e26e4001020">Operating System Version</a>



<a href="https://msdn.microsoft.com/aa7deebf-7dce-4147-8a15-1d7411aea0fa">System Information Functions</a>



<a href="https://msdn.microsoft.com/791bc6bf-f486-4110-b6ea-30a0935040b2">VerifyVersionInfo</a>



<a href="https://msdn.microsoft.com/2FAF67CD-CEEA-4096-B482-F5E2DF8D6C34">Version Helper functions</a>
 

 

