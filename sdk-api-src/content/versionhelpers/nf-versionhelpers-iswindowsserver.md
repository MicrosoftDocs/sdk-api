---
UID: NF:versionhelpers.IsWindowsServer
title: IsWindowsServer function (versionhelpers.h)
author: windows-sdk-content
description: Indicates if the current OS is a Windows Server release.
old-location: base\iswindowsserver.htm
tech.root: SysInfo
ms.assetid: 7CC1DD25-762B-489F-AC20-1B57764923A2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IsWindowsServer, IsWindowsServer function, base.iswindowsserver, versionhelpers/IsWindowsServer
ms.topic: function
f1_keywords: 
 - "versionhelpers/IsWindowsServer"
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
 - IsWindowsServer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IsWindowsServer function


## -description


Indicates if the current OS is a  Windows Server release.  Applications that need to distinguish between server and client versions of Windows should call this function.


## -parameters






## -returns



True if the current OS is a Windows Server version; otherwise, false.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindows7orgreater">IsWindows7OrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindows7sp1orgreater">IsWindows7SP1OrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindows8orgreater">IsWindows8OrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindows8point1orgreater">IsWindows8Point1OrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsvistaorgreater">IsWindowsVistaOrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsvistasp1orgreater">IsWindowsVistaSP1OrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsvistasp2orgreater">IsWindowsVistaSP2OrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsxporgreater">IsWindowsXPOrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsxpsp1orgreater">IsWindowsXPSP1OrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsxpsp2orgreater">IsWindowsXPSP2OrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsxpsp3orgreater">IsWindowsXPSP3OrGreater</a>
 

 

