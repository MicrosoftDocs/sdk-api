---
UID: NF:winreg.RegDeleteKeyA
title: RegDeleteKeyA function (winreg.h)
description: Deletes a subkey and its values. (ANSI)
helpviewer_keywords: ["RegDeleteKeyA", "winreg/RegDeleteKeyA"]
old-location: base\regdeletekey.htm
tech.root: winprog
ms.assetid: a2310ca0-1b9f-48d1-a3b5-ea3a528bfaba
ms.date: 12/05/2018
ms.keywords: RegDeleteKey, RegDeleteKey function, RegDeleteKeyA, RegDeleteKeyW, _win32_regdeletekey, base.regdeletekey, winreg/RegDeleteKey, winreg/RegDeleteKeyA, winreg/RegDeleteKeyW
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegDeleteKeyW (Unicode) and RegDeleteKeyA (ANSI)
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
 - RegDeleteKeyA
 - winreg/RegDeleteKeyA
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
 - API-MS-Win-Deprecated-apis-advapi-l1-1-0.dll
 - API-MS-Win-Core-Registry-l2-2-0.dll
 - kernel32.dll
api_name:
 - RegDeleteKey
 - RegDeleteKeyA
 - RegDeleteKeyW
---

# RegDeleteKeyA function


## -description

Deletes a subkey and its values. Note that key names are not case sensitive.

<b>64-bit Windows:  </b>On WOW64, 32-bit applications view a registry tree that is separate from the registry tree that 64-bit applications view. To enable an application to delete an entry in the alternate registry view, use the <a href="/windows/desktop/api/winreg/nf-winreg-regdeletekeyexa">RegDeleteKeyEx</a> function.

## -parameters

### -param hKey [in]

A handle to an open registry key. The access rights of this key do not affect the delete operation. For more information about access rights, see 
<a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.

This handle is returned by the 
<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a> or 
<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a> function, or it can be one of the following 
<a href="/windows/desktop/SysInfo/predefined-keys">Predefined Keys</a>:<dl>
<dd><b>HKEY_CLASSES_ROOT</b></dd>
<dd><b>HKEY_CURRENT_CONFIG</b></dd>
<dd><b>HKEY_CURRENT_USER</b></dd>
<dd><b>HKEY_LOCAL_MACHINE</b></dd>
<dd><b>HKEY_USERS</b></dd>
</dl>

### -param lpSubKey [in]

The name of the key to be deleted. It must be a subkey of the key that <i>hKey</i> identifies, but it cannot have subkeys. This parameter cannot be <b>NULL</b>.

The function opens the subkey with the DELETE access right. 

Key names are not case sensitive.

For more information, see 
<a href="/windows/desktop/SysInfo/registry-element-size-limits">Registry Element Size Limits</a>.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. To get a generic description of the error, you can use the 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag.

## -remarks

A deleted key is not removed until the last handle to it is closed.

The subkey to be deleted must not have subkeys. To delete a key and all its subkeys, you need to enumerate the subkeys and delete them individually. To delete keys recursively, use the 
<a href="/windows/desktop/api/winreg/nf-winreg-regdeletetreea">RegDeleteTree</a> or <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shdeletekeya">SHDeleteKey</a> function.


#### Examples

For an example that uses this function, see <a href="/windows/desktop/SysInfo/deleting-a-key-with-subkeys">Deleting a Key with Subkeys</a>.

<div class="code"></div>

> [!NOTE] 
> On legacy versions of Windows, this API is also exposed by kernel32.dll.


> [!NOTE]
> The winreg.h header defines RegDeleteKey as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regclosekey">RegCloseKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regdeletetreea">RegDeleteTree</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="/windows/desktop/SysInfo/registry">Registry Overview</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shdeleteemptykeya">SHDeleteEmptyKey</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shdeletekeya">SHDeleteKey</a>
