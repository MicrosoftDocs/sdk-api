---
UID: NF:winreg.RegDisablePredefinedCacheEx
title: RegDisablePredefinedCacheEx function (winreg.h)
description: Disables handle caching for all predefined registry handles for the current process.
old-location: base\regdisablepredefinedcacheex.htm
tech.root: SysInfo
ms.assetid: a56cf7d9-0ac4-4719-af41-3c0cdcef6faf
ms.date: 12/05/2018
ms.keywords: RegDisablePredefinedCacheEx, RegDisablePredefinedCacheEx function, base.regdisablepredefinedcacheex, winreg/RegDisablePredefinedCacheEx
f1_keywords:
- winreg/RegDisablePredefinedCacheEx
dev_langs:
- c++
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Advapi32.dll
- API-MS-Win-Core-Localregistry-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-Registry-l1-1-0.dll
- API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
- API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
- MinKernelBase.dll
- api-ms-win-core-registry-l1-1-1.dll
api_name:
- RegDisablePredefinedCacheEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RegDisablePredefinedCacheEx function


## -description


Disables handle caching for all predefined registry handles for the current process.


## -parameters






## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a 
<a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a>.




## -remarks



This function does not work on a remote computer.

Services that change impersonation should call this function before using any of the predefined handles.

For example, any access of <b>HKEY_CURRENT_USER</b> after this function is called results in open and close operations being performed on <b>HKEY_USERS</b>\<b>SID_of_current_user</b>, or on <b>HKEY_USERS\.DEFAULT</b> if the current user's hive is not loaded. For more information on SIDs, see 
<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/security-identifiers">Security Identifiers</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/predefined-keys">Predefined Keys</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/registry-functions">Registry Functions</a>
 

 

