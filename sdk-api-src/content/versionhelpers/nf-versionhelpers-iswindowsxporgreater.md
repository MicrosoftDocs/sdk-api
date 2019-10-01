---
UID: NF:versionhelpers.IsWindowsXPOrGreater
title: IsWindowsXPOrGreater function (versionhelpers.h)
author: windows-sdk-content
description: Indicates if the current OS version matches, or is greater than, the Windows XP version.
old-location: base\iswindowsxporgreater.htm
tech.root: SysInfo
ms.assetid: 48B7FAD6-569F-4CF5-A413-857679363736
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IsWindowsXPOrGreater, IsWindowsXPOrGreater function, base.iswindowsxporgreater, versionhelpers/IsWindowsXPOrGreater
ms.topic: function
f1_keywords: 
 - "versionhelpers/IsWindowsXPOrGreater"
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
 - IsWindowsXPOrGreater
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IsWindowsXPOrGreater function


## -description


Indicates if the current OS version matches, or is greater than, the Windows XP version. 


## -parameters






## -returns



True if the current OS version matches, or is greater than, the Windows XP version; otherwise, false.




## -remarks



This function does not differentiate between client and server releases.  It will return <b>true</b> if the current OS version number is equal to or higher than the version of the client named in the call. For example, a call to <a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsxpsp3orgreater">IsWindowsXPSP3OrGreater</a> will return <b>true</b> on Windows Server 2008. Applications that need to distinguish between server and client versions of Windows should call <a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsserver">IsWindowsServer</a>.

For situations where a Windows Server version number isn't shared with a Windows client release, you can use <a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsversionorgreater">IsWindowsVersionOrGreater</a> to confirm.


#### Examples

The inline functions defined in the <b>VersionHelpers.h</b> header file let you verify the operating system version by returning a <b>Boolean</b> value when testing for a version of Windows.

For example, if your application requires Windows XP or later, use the following test.


```cpp
#include <VersionHelpers.h>
…
    if (!IsWindowsXPOrGreater())
    {
       MessageBox(NULL, "You need at least Windows XP", "Version Not Supported", MB_OK);
    }

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindows7orgreater">IsWindows7OrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindows7sp1orgreater">IsWindows7SP1OrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindows8orgreater">IsWindows8OrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindows8point1orgreater">IsWindows8Point1OrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsserver">IsWindowsServer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsvistaorgreater">IsWindowsVistaOrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsvistasp1orgreater">IsWindowsVistaSP1OrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsvistasp2orgreater">IsWindowsVistaSP2OrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsxpsp1orgreater">IsWindowsXPSP1OrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsxpsp2orgreater">IsWindowsXPSP2OrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsxpsp3orgreater">IsWindowsXPSP3OrGreater</a>
 

 

