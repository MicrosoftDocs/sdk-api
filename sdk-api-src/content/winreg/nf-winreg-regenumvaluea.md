---
UID: NF:winreg.RegEnumValueA
title: RegEnumValueA function (winreg.h)
description: Enumerates the values for the specified open registry key. The function copies one indexed value name and data block for the key each time it is called. (ANSI)
helpviewer_keywords: ["RegEnumValueA", "winreg/RegEnumValueA"]
old-location: base\regenumvalue.htm
tech.root: winprog
ms.assetid: 7014ff96-c655-486f-af32-180b87281b06
ms.date: 12/05/2018
ms.keywords: RegEnumValue, RegEnumValue function, RegEnumValueA, RegEnumValueW, _win32_regenumvalue, base.regenumvalue, winreg/RegEnumValue, winreg/RegEnumValueA, winreg/RegEnumValueW
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegEnumValueW (Unicode) and RegEnumValueA (ANSI)
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
 - RegEnumValueA
 - winreg/RegEnumValueA
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
 - RegEnumValue
 - RegEnumValueA
 - RegEnumValueW
---

# RegEnumValueA function


## -description

Enumerates the values for the specified open registry key. The function copies one indexed value name and data block for the key each time it is called.

## -parameters

### -param hKey [in]

A handle to an open registry key. The key must have been opened with the KEY_QUERY_VALUE access right. For more information, see 
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

The index of the value to be retrieved. This parameter should be zero for the first call to the 
<b>RegEnumValue</b> function and then be incremented for subsequent calls. 




Because values are not ordered, any new value will have an arbitrary index. This means that the function may return values in any order.

### -param lpValueName [out]

A pointer to a buffer that receives the name of the value as a <b>null</b>-terminated string. 


This buffer must be large enough to include the terminating <b>null</b> character. 

For more information, see 
<a href="/windows/desktop/SysInfo/registry-element-size-limits">Registry Element Size Limits</a>.

### -param lpcchValueName [in, out]

A pointer to a variable that specifies the size of the buffer pointed to by the <i>lpValueName</i> parameter, in characters. When the function returns, the variable receives the number of characters stored in the buffer, not including the terminating <b>null</b> character.

If the buffer specified by <i>lpValueName</i> is not large enough to hold the data, the function returns ERROR_MORE_DATA and the buffer size in the variable pointed to by <i>lpValueName</i> is not changed. In this case, the contents of <i>lpcchValueName</i> are undefined.

Registry value names are limited to 32,767 bytes. The ANSI version of this function treats this parameter as a <b>SHORT</b> value. Therefore, if you specify a value greater than 32,767 bytes, there is an overflow and the function may return ERROR_MORE_DATA.

### -param lpReserved

This parameter is reserved and must be <b>NULL</b>.

### -param lpType [out, optional]

A pointer to a variable that receives a code indicating the type of data stored in the specified value. For a list of the possible type codes, see 
<a href="/windows/desktop/SysInfo/registry-value-types">Registry Value Types</a>. The <i>lpType</i> parameter can be <b>NULL</b> if the type code is not required.

### -param lpData [out, optional]

A pointer to a buffer that receives the data for the value entry. This parameter can be <b>NULL</b> if the data is not required. 




If <i>lpData</i> is <b>NULL</b> and <i>lpcbData</i> is non-<b>NULL</b>, the function stores the size of the data, in bytes, in the variable pointed to by <i>lpcbData</i>. This enables an application to determine the best way to allocate a buffer for the data.

### -param lpcbData [in, out, optional]

A pointer to a variable that specifies the size of the buffer pointed to by the <i>lpData</i> parameter, in bytes. When the function returns, the variable receives the number of bytes stored in the buffer. 

This parameter can be <b>NULL</b> only if <i>lpData</i> is <b>NULL</b>.

If the data has the REG_SZ, REG_MULTI_SZ or REG_EXPAND_SZ type, this size includes any terminating <b>null</b> character or characters. For more information, see Remarks.

If the buffer specified by <i>lpData</i> is not large enough to hold the data, the function returns ERROR_MORE_DATA and stores the required buffer size in the variable pointed to by <i>lpcbData</i>. In this case, the contents of <i>lpData</i> are undefined.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>. If there are no more values available, the function returns ERROR_NO_MORE_ITEMS.

If the buffer specified by <i>lpValueName</i> or <i>lpData</i> is too small to receive the value, the function returns ERROR_MORE_DATA.

## -remarks

To enumerate values, an application should initially call the 
<b>RegEnumValue</b> function with the <i>dwIndex</i> parameter set to zero. The application should then increment <i>dwIndex</i> and call the 
<b>RegEnumValue</b> function until there are no more values (until the function returns ERROR_NO_MORE_ITEMS).

The application can also set <i>dwIndex</i> to the index of the last value on the first call to the function and decrement the index until the value with index 0 is enumerated. To retrieve the index of the last value, use the 
<a href="/windows/desktop/api/winreg/nf-winreg-regqueryinfokeya">RegQueryInfoKey</a> function.

While using 
<b>RegEnumValue</b>, an application should not call any registry functions that might change the key being queried.

If the data has the REG_SZ, REG_MULTI_SZ or REG_EXPAND_SZ type, the string may not have been stored with the proper <b>null</b>-terminating characters.  Therefore, even if the function returns ERROR_SUCCESS, the application should ensure that the string is properly terminated before using it; otherwise, it may overwrite a buffer. (Note that REG_MULTI_SZ strings should have two <b>null</b>-terminating characters.)

To determine the maximum size of the name and data buffers, use the 
<a href="/windows/desktop/api/winreg/nf-winreg-regqueryinfokeya">RegQueryInfoKey</a> function.

> [!NOTE] 
> On legacy versions of Windows, this API is also exposed by kernel32.dll.

#### Examples

For an example, see 
<a href="/windows/desktop/SysInfo/enumerating-registry-subkeys">Enumerating Registry Subkeys</a>.

<div class="code"></div>




> [!NOTE]
> The winreg.h header defines RegEnumValue as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regenumkeyexa">RegEnumKeyEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regqueryinfokeya">RegQueryInfoKey</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="/windows/desktop/SysInfo/registry">Registry Overview</a>
