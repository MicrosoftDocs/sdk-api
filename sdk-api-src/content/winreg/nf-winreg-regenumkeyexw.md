---
UID: NF:winreg.RegEnumKeyExW
title: RegEnumKeyExW function (winreg.h)
description: Enumerates the subkeys of the specified open registry key. The function retrieves information about one subkey each time it is called. (Unicode)
helpviewer_keywords: ["RegEnumKeyEx", "RegEnumKeyEx function", "RegEnumKeyExW", "_win32_regenumkeyex", "base.regenumkeyex", "winreg/RegEnumKeyEx", "winreg/RegEnumKeyExW"]
old-location: base\regenumkeyex.htm
tech.root: winprog
ms.assetid: 647d34cc-01ba-4389-be29-b099ed198e7c
ms.date: 12/05/2018
ms.keywords: RegEnumKeyEx, RegEnumKeyEx function, RegEnumKeyExA, RegEnumKeyExW, _win32_regenumkeyex, base.regenumkeyex, winreg/RegEnumKeyEx, winreg/RegEnumKeyExA, winreg/RegEnumKeyExW
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegEnumKeyExW (Unicode) and RegEnumKeyExA (ANSI)
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
 - RegEnumKeyExW
 - winreg/RegEnumKeyExW
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
 - RegEnumKeyEx
 - RegEnumKeyExA
 - RegEnumKeyExW
---

# RegEnumKeyExW function


## -description

Enumerates the subkeys of the specified open registry key. The function retrieves information about one subkey each time it is called.

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
<dd><b>HKEY_PERFORMANCE_DATA</b></dd>
<dd><b>HKEY_USERS</b></dd>
</dl>

### -param dwIndex [in]

The index of the subkey to retrieve. This parameter should be zero for the first call to the 
<b>RegEnumKeyEx</b> function and then incremented for subsequent calls. 




Because subkeys are not ordered, any new subkey will have an arbitrary index. This means that the function may return subkeys in any order.

### -param lpName [out]

A pointer to a buffer that receives the name of the subkey, including the terminating <b>null</b> character. The function copies only the name of the subkey, not the full key hierarchy, to the buffer. 


If the function fails, no information is copied to this buffer.

For more information, see 
<a href="/windows/desktop/SysInfo/registry-element-size-limits">Registry Element Size Limits</a>.

### -param lpcchName [in, out]

A pointer to a variable that specifies the size of the buffer specified by the <i>lpName</i> parameter, in characters. This size should include the terminating <b>null</b> character. If the function succeeds, the variable pointed to by <i>lpcName</i> contains the number of characters stored in the buffer, not including the terminating <b>null</b> character.

To determine the required buffer size, use the 
<a href="/windows/desktop/api/winreg/nf-winreg-regqueryinfokeya">RegQueryInfoKey</a> function to determine the size of the largest subkey for the key identified by the <i>hKey</i> parameter.

### -param lpReserved

This parameter is reserved and must be <b>NULL</b>.

### -param lpClass [in, out]

A pointer to a buffer that receives the user-defined class of the enumerated subkey. This parameter can be <b>NULL</b>.

### -param lpcchClass [in, out, optional]

A pointer to a variable that specifies the size of the buffer specified by the <i>lpClass</i> parameter, in characters. The size should include the terminating <b>null</b> character. If the function succeeds, <i>lpcClass</i> contains the number of characters stored in the buffer, not including the terminating <b>null</b> character. This parameter can be <b>NULL</b> only if <i>lpClass</i> is <b>NULL</b>.

### -param lpftLastWriteTime [out, optional]

A pointer to <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that receives the time at which the enumerated subkey was last written. This parameter can be <b>NULL</b>.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>. If there are no more subkeys available, the function returns ERROR_NO_MORE_ITEMS.

If the <i>lpName</i> buffer is too small to receive the name of the key, the function returns ERROR_MORE_DATA.

## -remarks

To enumerate subkeys, an application should initially call the 
<b>RegEnumKeyEx</b> function with the <i>dwIndex</i> parameter set to zero. The application should then increment the <i>dwIndex</i> parameter and call 
<b>RegEnumKeyEx</b> until there are no more subkeys (meaning the function returns ERROR_NO_MORE_ITEMS).

The application can also set <i>dwIndex</i> to the index of the last subkey on the first call to the function and decrement the index until the subkey with the index 0 is enumerated. To retrieve the index of the last subkey, use the 
<a href="/windows/desktop/api/winreg/nf-winreg-regqueryinfokeya">RegQueryInfoKey</a> function.

While an application is using the 
<b>RegEnumKeyEx</b> function, it should not make calls to any registration functions that might change the key being enumerated.

Note that operations that access certain registry keys are redirected. For more information,  see <a href="/windows/desktop/SysInfo/registry-virtualization">Registry Virtualization</a> and <a href="/windows/desktop/SysInfo/32-bit-and-64-bit-application-data-in-the-registry">32-bit and 64-bit Application Data in the Registry</a>.


#### Examples

For an example, see 
<a href="/windows/desktop/SysInfo/enumerating-registry-subkeys">Enumerating Registry Subkeys</a>.

<div class="code"></div>




> [!NOTE]
> The winreg.h header defines RegEnumKeyEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regdeletekeya">RegDeleteKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regqueryinfokeya">RegQueryInfoKey</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="/windows/desktop/SysInfo/registry">Registry Overview</a>
