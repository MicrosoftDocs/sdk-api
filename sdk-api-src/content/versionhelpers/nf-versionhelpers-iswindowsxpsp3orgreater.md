---
UID: NF:versionhelpers.IsWindowsXPSP3OrGreater
title: IsWindowsXPSP3OrGreater function (versionhelpers.h)
description: Indicates if the current OS version matches, or is greater than, the Windows XP with Service Pack 3 (SP3) version.
helpviewer_keywords: ["IsWindowsXPSP3OrGreater","IsWindowsXPSP3OrGreater function","base.iswindowsxpsp3orgreater","versionhelpers/IsWindowsXPSP3OrGreater"]
old-location: base\iswindowsxpsp3orgreater.htm
tech.root: winprog
ms.assetid: 06DC8FF0-8652-4652-855F-600AC53C6301
ms.date: 12/05/2018
ms.keywords: IsWindowsXPSP3OrGreater, IsWindowsXPSP3OrGreater function, base.iswindowsxpsp3orgreater, versionhelpers/IsWindowsXPSP3OrGreater
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsWindowsXPSP3OrGreater
 - versionhelpers/IsWindowsXPSP3OrGreater
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - ntdll.dll
api_name:
 - IsWindowsXPSP3OrGreater
---

# IsWindowsXPSP3OrGreater function


## -description

Indicates if the current OS version matches, or is greater than, the Windows XP with Service Pack 3 (SP3) version.



## -returns

True if the current OS version matches, or is greater than, the Windows XP with SP3 version; otherwise, false.

## -remarks

This function does not differentiate between client and server releases.  It will return <b>true</b> if the current OS version number is equal to or higher than the version of the client named in the call. For example, a call to <b>IsWindowsXPSP3OrGreater</b> will return <b>true</b> on Windows Server 2008. Applications that need to distinguish between server and client versions of Windows should call <a href="/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsserver">IsWindowsServer</a>.

For situations where a Windows Server version number isn't shared with a Windows client release, you can use <a href="/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsversionorgreater">IsWindowsVersionOrGreater</a> to confirm.


#### Examples

The inline functions defined in the <b>VersionHelpers.h</b> header file let you verify the operating system version by returning a <b>Boolean</b> value when testing for a version of Windows.

For example, if your application requires Windows XP with SP3 or later, use the following test.


```cpp
#include <VersionHelpers.h>
…
    if (!IsWindowsXPSP3OrGreater())
    {
       MessageBox(NULL, "You need at least Windows XP with SP3", "Version Not Supported", MB_OK);
    }

```

## -see-also

<a href="/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindows7orgreater">IsWindows7OrGreater</a>



<a href="/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindows7sp1orgreater">IsWindows7SP1OrGreater</a>



<a href="/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindows8orgreater">IsWindows8OrGreater</a>



<a href="/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindows8point1orgreater">IsWindows8Point1OrGreater</a>



<a href="/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsserver">IsWindowsServer</a>



<a href="/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsvistaorgreater">IsWindowsVistaOrGreater</a>



<a href="/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsvistasp1orgreater">IsWindowsVistaSP1OrGreater</a>



<a href="/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsvistasp2orgreater">IsWindowsVistaSP2OrGreater</a>



<a href="/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsxporgreater">IsWindowsXPOrGreater</a>



<a href="/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsxpsp1orgreater">IsWindowsXPSP1OrGreater</a>



<a href="/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsxpsp2orgreater">IsWindowsXPSP2OrGreater</a>
