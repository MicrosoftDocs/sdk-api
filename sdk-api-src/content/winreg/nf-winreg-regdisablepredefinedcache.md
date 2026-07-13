---
UID: NF:winreg.RegDisablePredefinedCache
title: RegDisablePredefinedCache function (winreg.h)
description: Disables handle caching of the predefined registry handle for HKEY_CURRENT_USER for the current process.
helpviewer_keywords: ["RegDisablePredefinedCache","RegDisablePredefinedCache function","_win32_regdisablepredefinedcache","base.regdisablepredefinedcache","winreg/RegDisablePredefinedCache"]
old-location: base\regdisablepredefinedcache.htm
tech.root: winprog
ms.assetid: 837584b3-5f61-4535-9e66-56f50ab3fa46
ms.date: 12/05/2018
ms.keywords: RegDisablePredefinedCache, RegDisablePredefinedCache function, _win32_regdisablepredefinedcache, base.regdisablepredefinedcache, winreg/RegDisablePredefinedCache
req.header: winreg.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegDisablePredefinedCache
 - winreg/RegDisablePredefinedCache
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-registry-l2-3-0.dll
 - Advapi32.dll
 - API-MS-Win-Core-Registry-l2-1-0.dll
 - advapi32legacy.dll
 - API-MS-Win-Core-Registry-l2-2-0.dll
api_name:
 - RegDisablePredefinedCache
---

# RegDisablePredefinedCache function


## -description

Disables handle caching of the predefined registry handle for <b>HKEY_CURRENT_USER</b> for the current process. This function does not work on a remote computer.

To disables handle caching of all predefined registry handles, use the <a href="/windows/desktop/api/winreg/nf-winreg-regdisablepredefinedcacheex">RegDisablePredefinedCacheEx</a> function.



## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

Any access of <b>HKEY_CURRENT_USER</b> after this function is called will result in operations being performed on <b>HKEY_USERS</b>&#92;<b>SID_of_current_user</b>,  or on <b>HKEY_USERS\.DEFAULT</b> if the current user's hive is not loaded. For more information on SIDs, see 
<a href="/windows/desktop/SecAuthZ/security-identifiers">Security Identifiers</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="/windows/desktop/SysInfo/predefined-keys">Predefined Keys</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regdisablepredefinedcacheex">RegDisablePredefinedCacheEx</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>
