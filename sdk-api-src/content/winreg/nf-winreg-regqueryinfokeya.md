---
UID: NF:winreg.RegQueryInfoKeyA
title: RegQueryInfoKeyA function (winreg.h)
description: Retrieves information about the specified registry key. (ANSI)
helpviewer_keywords: ["RegQueryInfoKeyA", "winreg/RegQueryInfoKeyA"]
old-location: base\regqueryinfokey.htm
tech.root: winprog
ms.assetid: 25eb2cd2-9fdd-4d6f-8071-daab56f9aae1
ms.date: 12/05/2018
ms.keywords: RegQueryInfoKey, RegQueryInfoKey function, RegQueryInfoKeyA, RegQueryInfoKeyW, _win32_regqueryinfokey, base.regqueryinfokey, winreg/RegQueryInfoKey, winreg/RegQueryInfoKeyA, winreg/RegQueryInfoKeyW
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegQueryInfoKeyW (Unicode) and RegQueryInfoKeyA (ANSI)
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
 - RegQueryInfoKeyA
 - winreg/RegQueryInfoKeyA
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
 - kernel32.dll
api_name:
 - RegQueryInfoKey
 - RegQueryInfoKeyA
 - RegQueryInfoKeyW
---

# RegQueryInfoKeyA function


## -description

Retrieves information about the specified registry key.

## -parameters

### -param hKey [in]

A handle to an open registry key. The key must have been opened with the KEY_QUERY_VALUE access right. For more information, see 
<a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>. 




This handle is returned by the 
<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>, <a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeytransacteda">RegCreateKeyTransacted</a>, <a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>, or 
<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeytransacteda">RegOpenKeyTransacted</a> function. It can also be one of the following 
<a href="/windows/desktop/SysInfo/predefined-keys">predefined keys</a>:<pre><b></b>
   <b>HKEY_CLASSES_ROOT</b>
   <b>HKEY_CURRENT_CONFIG</b>
   <b>HKEY_CURRENT_USER</b>
   <b>HKEY_LOCAL_MACHINE</b>
   <b>HKEY_PERFORMANCE_DATA</b>
   <b>HKEY_USERS</b></pre>

### -param lpClass [out, optional]

A pointer to a buffer that receives the user-defined class of the key. This parameter can be <b>NULL</b>.

### -param lpcchClass [in, out, optional]

A pointer to a variable that specifies the size of the buffer pointed to by the <i>lpClass</i> parameter, in characters. 

The size should include the terminating <b>null</b> character. When the function returns, this variable contains the size of the class string that is stored in the buffer. The count returned does not include the terminating <b>null</b> character. If the buffer is not big enough, the function returns ERROR_MORE_DATA, and the variable contains the size of the string, in characters, without counting the terminating <b>null</b> character.

If <i>lpClass</i> is <b>NULL</b>, <i>lpcClass</i> can be <b>NULL</b>.

If the <i>lpClass</i> parameter is a valid address, but the <i>lpcClass</i> parameter is not, for example, it is <b>NULL</b>, then the  function returns ERROR_INVALID_PARAMETER.

### -param lpReserved

This parameter is reserved and must be <b>NULL</b>.

### -param lpcSubKeys [out, optional]

A pointer to a variable that receives the number of subkeys that are contained by the specified key. This parameter can be <b>NULL</b>.

### -param lpcbMaxSubKeyLen [out, optional]

A pointer to a variable that receives the size of the key's subkey with the longest name, in ANSI characters, not including the terminating <b>null</b> character. This parameter can be <b>NULL</b>.

### -param lpcbMaxClassLen [out, optional]

A pointer to a variable that receives the size of the longest string that specifies a subkey class, in ANSI characters. The count returned does not include the terminating <b>null</b> character. This parameter can be <b>NULL</b>.

### -param lpcValues [out, optional]

A pointer to a variable that receives the number of values that are associated with the key. This parameter can be <b>NULL</b>.

### -param lpcbMaxValueNameLen [out, optional]

A pointer to a variable that receives the size of the key's longest value name, in ANSI characters. The size does not include the terminating <b>null</b> character. This parameter can be <b>NULL</b>.

### -param lpcbMaxValueLen [out, optional]

A pointer to a variable that receives the size of the longest data component among the key's values, in bytes. This parameter can be <b>NULL</b>.

### -param lpcbSecurityDescriptor [out, optional]

A pointer to a variable that receives the size of the key's security descriptor, in bytes. This parameter can be <b>NULL</b>.

### -param lpftLastWriteTime [out, optional]

A pointer to a 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that receives the last write time. This parameter can be <b>NULL</b>. 




The function sets the members of the 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure to indicate the last time that the key or any of its value entries is modified.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

If the <i>lpClass</i> buffer is too small to receive the name of the class, the function returns ERROR_MORE_DATA.

## -remarks

> [!NOTE] 
> On legacy versions of Windows, this API is also exposed by kernel32.dll.

## -see-also

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regdeletekeya">RegDeleteKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regenumkeyexa">RegEnumKeyEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regenumvaluea">RegEnumValue</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa">RegQueryValueEx</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="/windows/desktop/SysInfo/registry">Registry Overview</a>
