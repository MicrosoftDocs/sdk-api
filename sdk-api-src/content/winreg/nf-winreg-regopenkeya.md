---
UID: NF:winreg.RegOpenKeyA
title: RegOpenKeyA function (winreg.h)
description: Opens the specified registry key. (ANSI)
helpviewer_keywords: ["RegOpenKeyA", "winreg/RegOpenKeyA"]
old-location: base\regopenkey.htm
tech.root: winprog
ms.assetid: bad0a0f8-1889-4eff-98be-084c95d69f3b
ms.date: 12/05/2018
ms.keywords: RegOpenKey, RegOpenKey function, RegOpenKeyA, RegOpenKeyW, _win32_regopenkey, base.regopenkey, winreg/RegOpenKey, winreg/RegOpenKeyA, winreg/RegOpenKeyW
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegOpenKeyW (Unicode) and RegOpenKeyA (ANSI)
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
 - RegOpenKeyA
 - winreg/RegOpenKeyA
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
 - RegOpenKey
 - RegOpenKeyA
 - RegOpenKeyW
---

# RegOpenKeyA function


## -description

Opens the specified registry key.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should use the 
<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a> function.</div><div> </div>

## -parameters

### -param hKey [in]

A handle to an open registry key. This handle is returned by the 
<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a> or 
<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a> function, or it can be one of the following 
<a href="/windows/desktop/SysInfo/predefined-keys">predefined keys</a>:

* <b>HKEY_CLASSES_ROOT</b>
* <b>HKEY_CURRENT_CONFIG</b>
* <b>HKEY_CURRENT_USER</b>
* <b>HKEY_LOCAL_MACHINE</b>
* <b>HKEY_USERS</b>

### -param lpSubKey [in, optional]

The name of the registry key to be opened. This key must be a subkey of the key identified by the <i>hKey</i> parameter. 

Key names are not case sensitive.

If this parameter is <b>NULL</b> or a pointer to an empty string, the function returns the same handle that was passed in.

For more information, see 
<a href="/windows/desktop/SysInfo/registry-element-size-limits">Registry Element Size Limits</a>.

### -param phkResult [out]

A pointer to a variable that receives a handle to the opened key. If the key is not one of the predefined registry keys, call the 
<a href="/windows/desktop/api/winreg/nf-winreg-regclosekey">RegCloseKey</a> function after you have finished using the handle.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.

## -remarks

The 
<b>RegOpenKey</b> function uses the default security access mask to open a key. If opening the key requires a different access right, the function fails, returning ERROR_ACCESS_DENIED. An application should use the 
<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a> function to specify an access mask in this situation.

<b>RegOpenKey</b> does not create the specified key if the key does not exist in the database.

If your service or application impersonates different users, do not use this function with <b>HKEY_CURRENT_USER</b>. Instead, call the <a href="/windows/desktop/api/winreg/nf-winreg-regopencurrentuser">RegOpenCurrentUser</a> function.





> [!NOTE]
> The winreg.h header defines RegOpenKey as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regclosekey">RegCloseKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regdeletekeya">RegDeleteKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="/windows/desktop/SysInfo/registry">Registry Overview</a>
