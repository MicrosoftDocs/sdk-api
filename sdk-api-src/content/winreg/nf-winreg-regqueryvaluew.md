---
UID: NF:winreg.RegQueryValueW
title: RegQueryValueW function (winreg.h)
description: Retrieves the data associated with the default or unnamed value of a specified registry key. The data must be a null-terminated string. (Unicode)
helpviewer_keywords: ["RegQueryValue", "RegQueryValue function", "RegQueryValueW", "_win32_regqueryvalue", "base.regqueryvalue", "winreg/RegQueryValue", "winreg/RegQueryValueW"]
old-location: base\regqueryvalue.htm
tech.root: winprog
ms.assetid: 18f27717-3bd9-45ac-a1ea-61abc1753a52
ms.date: 12/05/2018
ms.keywords: RegQueryValue, RegQueryValue function, RegQueryValueA, RegQueryValueW, _win32_regqueryvalue, base.regqueryvalue, winreg/RegQueryValue, winreg/RegQueryValueA, winreg/RegQueryValueW
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegQueryValueW (Unicode) and RegQueryValueA (ANSI)
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
 - RegQueryValueW
 - winreg/RegQueryValueW
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
 - RegQueryValue
 - RegQueryValueA
 - RegQueryValueW
---

# RegQueryValueW function


## -description

Retrieves the data associated with the default or unnamed value of a specified registry key. The data must be a <b>null</b>-terminated string.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should use the 
<a href="/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa">RegQueryValueEx</a> function.</div><div> </div>

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
<dd><b>HKEY_USERS</b></dd>
</dl>

### -param lpSubKey [in, optional]

The name of the subkey of the <i>hKey</i> parameter for which the default value is retrieved. 

Key names are not case sensitive.

If this parameter is <b>NULL</b> or points to an empty string, the function retrieves the default value for the key identified by <i>hKey</i>.

For more information, see 
<a href="/windows/desktop/SysInfo/registry-element-size-limits">Registry Element Size Limits</a>.

### -param lpData [out, optional]

A pointer to a buffer that receives the default value of the specified key. 




If <i>lpValue</i> is <b>NULL</b>, and <i>lpcbValue</i> is non-<b>NULL</b>, the function returns ERROR_SUCCESS, and stores the size of the data, in bytes, in the variable pointed to by <i>lpcbValue</i>. This enables an application to determine the best way to allocate a buffer for the value's data.

### -param lpcbData [in, out, optional]

A pointer to a variable that specifies the size of the buffer pointed to by the <i>lpValue</i> parameter, in bytes. When the function returns, this variable contains the size of the data copied to <i>lpValue</i>, including any terminating <b>null</b> characters. 




If the data has the REG_SZ, REG_MULTI_SZ or REG_EXPAND_SZ type, this size includes any terminating <b>null</b> character or characters. For more information, see Remarks.

If the buffer specified <i>lpValue</i> is not large enough to hold the data, the function returns ERROR_MORE_DATA and stores the required buffer size in the variable pointed to by <i>lpcbValue</i>. In this case, the contents of the <i>lpValue</i> buffer are undefined.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

If the <i>lpValue</i> buffer is too small to receive the value, the function returns ERROR_MORE_DATA.

## -remarks

If the ANSI version of this function is used (either by explicitly calling <b>RegQueryValueA</b> or by not defining UNICODE before including the Windows.h file), this function converts the stored Unicode string to an ANSI string before copying it to the buffer specified by the <i>lpValue</i> parameter.

If the data has the REG_SZ, REG_MULTI_SZ or REG_EXPAND_SZ type, the string may not have been stored with the proper <b>null</b>-terminating characters.  Therefore, even if the function returns ERROR_SUCCESS, the application should ensure that the string is properly terminated before using it; otherwise, it may overwrite a buffer. (Note that REG_MULTI_SZ strings should have two <b>null</b>-terminating characters.)

Note that operations that access certain registry keys are redirected. For more information,  see <a href="/windows/desktop/SysInfo/registry-virtualization">Registry Virtualization</a> and <a href="/windows/desktop/SysInfo/32-bit-and-64-bit-application-data-in-the-registry">32-bit and 64-bit Application Data in the Registry</a>.





> [!NOTE]
> The winreg.h header defines RegQueryValue as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regenumkeyexa">RegEnumKeyEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regenumvaluea">RegEnumValue</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regqueryinfokeya">RegQueryInfoKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa">RegQueryValueEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regsetvalueexa">RegSetValueEx</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="/windows/desktop/SysInfo/registry">Registry Overview</a>
