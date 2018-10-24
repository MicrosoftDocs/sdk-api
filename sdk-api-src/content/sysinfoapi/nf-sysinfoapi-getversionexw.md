---
UID: NF:sysinfoapi.GetVersionExW
title: GetVersionExW function
author: windows-sdk-content
description: With the release of Windows 8.1, the behavior of the GetVersionEx API has changed in the value it will return for the operating system version. The value returned by the GetVersionEx function now depends on how the application is manifested.
old-location: base\getversionex.htm
tech.root: sysinfo
ms.assetid: 8e3ab4d6-bacd-4bc5-b8f6-dd49289354de
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetVersionEx, GetVersionEx function, GetVersionExA, GetVersionExW, _win32_getversionex, base.getversionex, sysinfoapi/GetVersionEx, sysinfoapi/GetVersionExA, sysinfoapi/GetVersionExW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetVersionExW function


## -description


<p class="CCE_Message">[<b>GetVersionEx</b> may be altered or unavailable for releases after Windows 8.1. Instead, use the <a href="https://msdn.microsoft.com/2FAF67CD-CEEA-4096-B482-F5E2DF8D6C34">Version Helper functions</a>]

With the release of Windows 8.1, the behavior of the <b>GetVersionEx</b> API has changed in the value it will return for the operating system version. The value returned by the <b>GetVersionEx</b> function now depends on how the application is manifested. 

Applications not manifested for Windows 8.1 or Windows 10 will return the Windows 8 OS version value (6.2).  Once an application is manifested for a given operating system version, <b>GetVersionEx</b> will always return the version that the application is manifested for in future releases.  To manifest your applications for Windows 8.1 or Windows 10, refer to <a href="https://msdn.microsoft.com/E7A1A16A-95B3-4B45-81AD-A19E33F15AE4">Targeting your application for Windows</a>.


## -parameters




### -param lpVersionInformation

TBD




#### - lpVersionInfo [in, out]

An 
<a href="https://msdn.microsoft.com/a173df17-dad2-4330-aa66-4ff789fd7cc2">OSVERSIONINFO</a> or <a href="https://msdn.microsoft.com/4ab07a72-404d-459b-b061-b3b06b5db37e">OSVERSIONINFOEX</a> structure that receives the operating system information. 




Before calling the 
<b>GetVersionEx</b> function, set the <b>dwOSVersionInfoSize</b> member of the structure as appropriate to indicate which data structure is being passed to this function.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The function fails if you specify an invalid value for the <b>dwOSVersionInfoSize</b> member of the 
<a href="https://msdn.microsoft.com/a173df17-dad2-4330-aa66-4ff789fd7cc2">OSVERSIONINFO</a> or 
<a href="https://msdn.microsoft.com/4ab07a72-404d-459b-b061-b3b06b5db37e">OSVERSIONINFOEX</a> structure.




## -remarks



Identifying the current operating system is usually not the best way to determine whether a particular operating system feature is present. This is because the operating system may have had new features added in a redistributable DLL. Rather than using 
<b>GetVersionEx</b> to determine the operating system platform or version number, test for the presence of the feature itself. For more information, see 
<a href="https://msdn.microsoft.com/1a70b1d9-ed66-4201-9921-4e26e4001020">Operating System Version</a>.

The <a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a> function provides additional information about the current operating system. 

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
 

To check for specific operating systems or operating system features, use the <a href="https://msdn.microsoft.com/827a76bc-3581-4f1c-8095-8e2fd30dfdbc">IsOS</a> function. The <a href="https://msdn.microsoft.com/711e6010-2068-4c97-9009-6ecdf54797b6">GetProductInfo</a> function retrieves the product type.

To retrieve information for the operating system on a remote computer, use the <a href="https://msdn.microsoft.com/08777069-1afd-4482-8090-c65ef0bec1ea">NetWkstaGetInfo</a> function, the <a href="https://msdn.microsoft.com/eb6a8cff-20a0-4211-b46a-3084e9c39246">Win32_OperatingSystem</a> WMI class, or the <a href="https://msdn.microsoft.com/c990b6bb-6256-4216-9435-c85c67db4d13">OperatingSystem</a> property of the <b>IADsComputer</b> interface.

To compare the current system version to a required version, use the 
<a href="https://msdn.microsoft.com/791bc6bf-f486-4110-b6ea-30a0935040b2">VerifyVersionInfo</a> function instead of using 
<b>GetVersionEx</b> to perform the comparison yourself.

If compatibility mode is in effect, the <b>GetVersionEx</b> function reports the operating system as it identifies itself, which may not be the operating system that is installed. For example, if compatibility mode is in effect, <b>GetVersionEx</b> reports the operating system that is selected for <a href="http://go.microsoft.com/fwlink/p/?linkid=115300">application compatibility</a>.


#### Examples

When using the 
<b>GetVersionEx</b> function to determine whether your application is running on a particular version of the operating system, check for version numbers that are greater than or equal to the desired version numbers. This ensures that the test succeeds for later versions of the operating system. For example, if your application requires Windows XP or later, use the following test.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;stdio.h&gt;

void main()
{
    OSVERSIONINFO osvi;
    BOOL bIsWindowsXPorLater;

    ZeroMemory(&amp;osvi, sizeof(OSVERSIONINFO));
    osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFO);

    GetVersionEx(&amp;osvi);

    bIsWindowsXPorLater = 
       ( (osvi.dwMajorVersion &gt; 5) ||
       ( (osvi.dwMajorVersion == 5) &amp;&amp; (osvi.dwMinorVersion &gt;= 1) ));

    if(bIsWindowsXPorLater)
        printf("The system meets the requirements.\n");
    else printf("The system does not meet the requirements.\n");
}
</pre>
</td>
</tr>
</table></span></div>
For an example that identifies the current operating system, see 
<a href="https://msdn.microsoft.com/ae851aef-27d5-4eb7-aeb2-ccdfbf040e5a">Getting the System Version</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/25cb87c6-e4a5-447e-8153-f12638859d00">GetVersion</a>



<a href="https://msdn.microsoft.com/a173df17-dad2-4330-aa66-4ff789fd7cc2">OSVERSIONINFO</a>



<a href="https://msdn.microsoft.com/4ab07a72-404d-459b-b061-b3b06b5db37e">OSVERSIONINFOEX</a>



<a href="https://msdn.microsoft.com/1a70b1d9-ed66-4201-9921-4e26e4001020">Operating System Version</a>



<a href="https://msdn.microsoft.com/aa7deebf-7dce-4147-8a15-1d7411aea0fa">System Information Functions</a>



<a href="https://msdn.microsoft.com/791bc6bf-f486-4110-b6ea-30a0935040b2">VerifyVersionInfo</a>



<a href="https://msdn.microsoft.com/2FAF67CD-CEEA-4096-B482-F5E2DF8D6C34">Version Helper functions</a>
 

 

