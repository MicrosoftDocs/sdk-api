---
UID: NF:versionhelpers.IsWindows8Point1OrGreater
title: IsWindows8Point1OrGreater function
author: windows-sdk-content
description: Indicates if the current OS version matches, or is greater than, the Windows 8.1 version.
old-location: base\iswindows8_1orgreater.htm
tech.root: sysinfo
ms.assetid: E391B568-5E43-42C7-B186-8CA524331FFE
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IsWindows8Point1OrGreater, IsWindows8Point1OrGreater function, base.iswindows8_1orgreater, versionhelpers/IsWindows8Point1OrGreater
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: versionhelpers.h
req.include-header: 
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
req.lib: Kernel32.lib; Ntdll.lib
req.dll: Kernel32.dll; Ntdll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - ntdll.dll
api_name:
 - IsWindows8Point1OrGreater
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IsWindows8Point1OrGreater function


## -description


Indicates if the current OS version matches, or is greater than, the Windows 8.1 version.


## -parameters






## -returns



True if the current OS version matches, or is greater than, the Windows 8.1 version; otherwise, false.




## -remarks



Applications not manifested for Windows 8.1 or Windows 10 return false, even if the current operating system version is Windows 8.1 or Windows 10. To manifest your applications for Windows 8.1 or Windows 10, see <a href="https://msdn.microsoft.com/E7A1A16A-95B3-4B45-81AD-A19E33F15AE4">Targeting your application for Windows</a>.


This function does not differentiate between client and server releases.  It will return <b>true</b> if the current OS version number is equal to or higher than the version of the client named in the call. For example, a call to <a href="https://msdn.microsoft.com/06DC8FF0-8652-4652-855F-600AC53C6301">IsWindowsXPSP3OrGreater</a> will return <b>true</b> on Windows Server 2008. Applications that need to distinguish between server and client versions of Windows should call <a href="https://msdn.microsoft.com/7CC1DD25-762B-489F-AC20-1B57764923A2">IsWindowsServer</a>.

For situations where a Windows Server version number isn't shared with a Windows client release, you can use <a href="https://msdn.microsoft.com/B28DFEC0-A94E-49F6-9DF0-4EE470EC4AF5">IsWindowsVersionOrGreater</a> to confirm.


#### Examples

The inline functions defined in the <b>VersionHelpers.h</b> header file let you verify the operating system version by returning a <b>Boolean</b> value when testing for a version of Windows.

For example, if your application requires Windows 8.1 or later, use the following test.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;VersionHelpers.h&gt;
…
    if (!IsWindows8Point1OrGreater())
    {
       MessageBox(NULL, "You need at least Windows 8.1", "Version Not Supported", MB_OK);
    }
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5C475B5E-1412-4F60-AB81-00BE83E204BF">IsWindows7OrGreater</a>



<a href="https://msdn.microsoft.com/E8AD3423-91EF-4ECE-9EF2-808C68CEA861">IsWindows7SP1OrGreater</a>



<a href="https://msdn.microsoft.com/D11971C8-2E8F-4AD2-BE0B-FEFEC8949125">IsWindows8OrGreater</a>



<a href="https://msdn.microsoft.com/7CC1DD25-762B-489F-AC20-1B57764923A2">IsWindowsServer</a>



<a href="https://msdn.microsoft.com/556C70DC-6A44-4D85-BDBF-C1110D63DC69">IsWindowsVistaOrGreater</a>



<a href="https://msdn.microsoft.com/7E74A761-E336-4618-B92F-166C3DF1FF66">IsWindowsVistaSP1OrGreater</a>



<a href="https://msdn.microsoft.com/8D7F5DA2-8927-4453-A5E3-35A345B099EC">IsWindowsVistaSP2OrGreater</a>



<a href="https://msdn.microsoft.com/48B7FAD6-569F-4CF5-A413-857679363736">IsWindowsXPOrGreater</a>



<a href="https://msdn.microsoft.com/F8921444-B13D-4522-84F2-4792F4F37EA5">IsWindowsXPSP1OrGreater</a>



<a href="https://msdn.microsoft.com/DA957BA8-AD28-4096-8BE5-B77CA55B9324">IsWindowsXPSP2OrGreater</a>



<a href="https://msdn.microsoft.com/06DC8FF0-8652-4652-855F-600AC53C6301">IsWindowsXPSP3OrGreater</a>
 

 

