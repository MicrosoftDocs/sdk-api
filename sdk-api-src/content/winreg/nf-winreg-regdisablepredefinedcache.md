---
UID: NF:winreg.RegDisablePredefinedCache
title: RegDisablePredefinedCache function
author: windows-sdk-content
description: Disables handle caching of the predefined registry handle for HKEY_CURRENT_USER for the current process.
old-location: base\regdisablepredefinedcache.htm
tech.root: SysInfo
ms.assetid: 837584b3-5f61-4535-9e66-56f50ab3fa46
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: RegDisablePredefinedCache, RegDisablePredefinedCache function, _win32_regdisablepredefinedcache, base.regdisablepredefinedcache, winreg/RegDisablePredefinedCache
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Core-Registry-l2-1-0.dll
 - advapi32legacy.dll
 - API-MS-Win-Core-Registry-l2-2-0.dll
api_name:
 - RegDisablePredefinedCache
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegDisablePredefinedCache function


## -description


Disables handle caching of the predefined registry handle for <b>HKEY_CURRENT_USER</b> for the current process. This function does not work on a remote computer.

To disables handle caching of all predefined registry handles, use the <a href="https://msdn.microsoft.com/a56cf7d9-0ac4-4719-af41-3c0cdcef6faf">RegDisablePredefinedCacheEx</a> function.


## -parameters






## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



Any access of <b>HKEY_CURRENT_USER</b> after this function is called will result in operations being performed on <b>HKEY_USERS</b>\<b>SID_of_current_user</b>,  or on <b>HKEY_USERS\.DEFAULT</b> if the current user's hive is not loaded. For more information on SIDs, see 
<a href="https://msdn.microsoft.com/en-us/library/Aa379571(v=VS.85).aspx">Security Identifiers</a>.




## -see-also




<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a>



<a href="https://msdn.microsoft.com/db747656-b414-4594-ad39-6b476799060c">Predefined Keys</a>



<a href="https://msdn.microsoft.com/a56cf7d9-0ac4-4719-af41-3c0cdcef6faf">RegDisablePredefinedCacheEx</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>
 

 

