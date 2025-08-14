---
UID: NF:winreg.RegEnumKeyW
title: RegEnumKeyW function (winreg.h)
description: Enumerates the subkeys of the specified open registry key. (RegEnumKeyW)
helpviewer_keywords: ["RegEnumKey", "RegEnumKey function", "RegEnumKeyW", "_win32_regenumkey", "base.regenumkey", "winreg/RegEnumKey", "winreg/RegEnumKeyW"]
old-location: base\regenumkey.htm
tech.root: winprog
ms.assetid: 18a05c60-6c6d-438f-9003-f07d688d86a3
ms.date: 12/05/2018
ms.keywords: RegEnumKey, RegEnumKey function, RegEnumKeyA, RegEnumKeyW, _win32_regenumkey, base.regenumkey, winreg/RegEnumKey, winreg/RegEnumKeyA, winreg/RegEnumKeyW
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegEnumKeyW (Unicode) and RegEnumKeyA (ANSI)
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
 - RegEnumKeyW
 - winreg/RegEnumKeyW
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
 - RegEnumKey
 - RegEnumKeyA
 - RegEnumKeyW
---

# RegEnumKeyW function


## -description

Enumerates the subkeys of the specified open registry key. The function retrieves the name of one subkey each time it is called.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should use the 
<a href="/windows/desktop/api/winreg/nf-winreg-regenumkeyexa">RegEnumKeyEx</a> function.</div><div> </div>

## -parameters

### -param hKey [in]

A handle to an open registry key. The key must have been opened with the KEY_ENUMERATE_SUB_KEYS access right. For more information, see 
<a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>. 




This handle is returned by the 
<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>, <a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeytransacteda">RegCreateKeyTransacted</a>, <a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>, or 
<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeytransacteda">RegOpenKeyTransacted</a> function. It can also be one of the following 
<a href="/windows/desktop/SysInfo/predefined-keys">predefined keys</a>:<dl>
<dd><b>HKEY_CLASSES_ROOT</b></dd>
<dd><b>HKEY_CURRENT_CONFIG</b></dd>
<dd><b>HKEY_CURRENT_USER</b></dd>
<dd><b>HKEY_LOCAL_MACHINE</b></dd>
<dd><b>HKEY_USERS</b></dd>
</dl>

### -param dwIndex [in]

The index of the subkey of <i>hKey</i> to be retrieved. This value should be zero for the first call to the 
<b>RegEnumKey</b> function and then incremented for subsequent calls. 




Because subkeys are not ordered, any new subkey will have an arbitrary index. This means that the function may return subkeys in any order.

### -param lpName [out]

A pointer to a buffer that receives the name of the subkey, including the terminating null character. This function copies only the name of the subkey, not the full key hierarchy, to the buffer. 




For more information, see 
<a href="/windows/desktop/SysInfo/registry-element-size-limits">Registry Element Size Limits</a>.

### -param cchName [in]

The size of the buffer pointed to by the <i>lpName</i> parameter, in <b>TCHARs</b>. To determine the required buffer size, use the 
<a href="/windows/desktop/api/winreg/nf-winreg-regqueryinfokeya">RegQueryInfoKey</a> function to determine the size of the largest subkey for the key identified by the <i>hKey</i> parameter.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>. If there are no more subkeys available, the function returns ERROR_NO_MORE_ITEMS.

If the <i>lpName</i> buffer is too small to receive the name of the key, the function returns ERROR_MORE_DATA.

## -remarks

To enumerate subkeys, an application should initially call the 
<b>RegEnumKey</b> function with the <i>dwIndex</i> parameter set to zero. The application should then increment the <i>dwIndex</i> parameter and call the 
<b>RegEnumKey</b> function until there are no more subkeys (meaning the function returns ERROR_NO_MORE_ITEMS).

The application can also set <i>dwIndex</i> to the index of the last key on the first call to the function and decrement the index until the subkey with index 0 is enumerated. To retrieve the index of the last subkey, use the 
<a href="/windows/desktop/api/winreg/nf-winreg-regqueryinfokeya">RegQueryInfoKey</a>.

While an application is using the 
<b>RegEnumKey</b> function, it should not make calls to any registration functions that might change the key being queried.





> [!NOTE]
> The winreg.h header defines RegEnumKey as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regclosekey">RegCloseKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regdeletekeya">RegDeleteKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regenumkeyexa">RegEnumKeyEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regqueryinfokeya">RegQueryInfoKey</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="/windows/desktop/SysInfo/registry">Registry Overview</a>
