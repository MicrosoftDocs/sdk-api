---
UID: NF:winbase.GetSystemRegistryQuota
title: GetSystemRegistryQuota function (winbase.h)
author: windows-sdk-content
description: Retrieves the current size of the registry and the maximum size that the registry is allowed to attain on the system.
old-location: base\getsystemregistryquota.htm
tech.root: SysInfo
ms.assetid: 06687b2a-2dab-4102-8022-4b70677064b2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSystemRegistryQuota, GetSystemRegistryQuota function, base.getsystemregistryquota, winbase/GetSystemRegistryQuota
ms.topic: function
f1_keywords: 
 - "winbase/GetSystemRegistryQuota"
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
api_name:
 - GetSystemRegistryQuota
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetSystemRegistryQuota function


## -description


Retrieves the current size of the registry and the  maximum size that the registry is allowed to attain on the system.


## -parameters




### -param pdwQuotaAllowed [out, optional]

A pointer to a variable that receives the maximum size that the registry is allowed to attain on this system, in bytes.


### -param pdwQuotaUsed [out, optional]

A pointer to a variable that receives the current size of  the registry, in bytes.


## -returns



If the function succeeds, the return value is nonzero. 

If the function fails, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



To compile an application that uses this function, define _WIN32_WINNT as 0x0501 or later. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SysInfo/system-information-functions">System Information Functions</a>
 

 

