---
UID: NF:winreg.RegOpenCurrentUser
title: RegOpenCurrentUser function (winreg.h)
description: Retrieves a handle to the HKEY_CURRENT_USER key for the user the current thread is impersonating.
helpviewer_keywords: ["RegOpenCurrentUser","RegOpenCurrentUser function","_win32_regopencurrentuser","base.regopencurrentuser","winreg/RegOpenCurrentUser"]
old-location: base\regopencurrentuser.htm
tech.root: winprog
ms.assetid: 10a8cbfb-52dc-436a-827e-78f12eb62af0
ms.date: 12/05/2018
ms.keywords: RegOpenCurrentUser, RegOpenCurrentUser function, _win32_regopencurrentuser, base.regopencurrentuser, winreg/RegOpenCurrentUser
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
 - RegOpenCurrentUser
 - winreg/RegOpenCurrentUser
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-registry-l1-1-2.dll
 - Advapi32.dll
 - API-MS-Win-Core-Localregistry-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Registry-l1-1-0.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - MinKernelBase.dll
 - api-ms-win-core-registry-l1-1-1.dll
api_name:
 - RegOpenCurrentUser
---

# RegOpenCurrentUser function


## -description

Retrieves a handle to the <b>HKEY_CURRENT_USER</b> key for the user the current thread is impersonating.

## -parameters

### -param samDesired [in]

A mask that specifies the desired access rights to the key. The function fails if the security descriptor of the key does not permit the requested access for the calling process. For more information, see 
<a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.

### -param phkResult [out]

A pointer to a variable that receives a handle to the opened key. When you no longer need the returned handle, call the 
<a href="/windows/desktop/api/winreg/nf-winreg-regclosekey">RegCloseKey</a> function to close it.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.

## -remarks

The <b>HKEY_CURRENT_USER</b> key maps to the root of the current user's branch in the <b>HKEY_USERS</b> key. It is cached for all threads in a process. Therefore, this value does not change when another user's profile is loaded. 
<b>RegOpenCurrentUser</b> uses the thread's token to access the appropriate key, or the default if the profile is not loaded.

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regclosekey">RegCloseKey</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="/windows/desktop/SysInfo/registry">Registry Overview</a>