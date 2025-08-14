---
UID: NF:winreg.RegSetValueExA
title: RegSetValueExA function (winreg.h)
description: Sets the data and type of a specified value under a registry key. (ANSI)
helpviewer_keywords: ["RegSetValueExA", "winreg/RegSetValueExA"]
old-location: base\regsetvalueex.htm
tech.root: winprog
ms.assetid: 29b0e27c-4999-4e92-bd8b-bba74920bccc
ms.date: 12/05/2018
ms.keywords: RegSetValueEx, RegSetValueEx function, RegSetValueExA, RegSetValueExW, _win32_regsetvalueex, base.regsetvalueex, winreg/RegSetValueEx, winreg/RegSetValueExA, winreg/RegSetValueExW
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegSetValueExW (Unicode) and RegSetValueExA (ANSI)
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
 - RegSetValueExA
 - winreg/RegSetValueExA
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
 - RegSetValueEx
 - RegSetValueExA
 - RegSetValueExW
---

# RegSetValueExA function


## -description

Sets the data and type of a specified value under a registry key.

## -parameters

### -param hKey [in]

A handle to an open registry key. The key must have been opened with the KEY_SET_VALUE access right. For more information, see 
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
</dl>The Unicode version of this function supports the following additional predefined keys:<ul>
<li><b>HKEY_PERFORMANCE_TEXT</b></li>
<li><b>HKEY_PERFORMANCE_NLSTEXT</b></li>
</ul>

### -param lpValueName [in, optional]

The name of the value to be set. If a value with this name is not already present in the key, the function adds it to the key. 

If <i>lpValueName</i> is <b>NULL</b> or an empty string, "", the function sets the type and data for the key's unnamed or default value.

For more information, see 
<a href="/windows/desktop/SysInfo/registry-element-size-limits">Registry Element Size Limits</a>.

Registry keys do not have default values, but they can have one unnamed value, which can be of any type.

### -param Reserved

This parameter is reserved and must be zero.

### -param dwType [in]

The type of data pointed to by the <i>lpData</i> parameter. For a list of the possible types, see 
<a href="/windows/desktop/SysInfo/registry-value-types">Registry Value Types</a>.

### -param lpData [in]

The data to be stored. 

For string-based types, such as REG_SZ, the string must be <b>null</b>-terminated. With the REG_MULTI_SZ data type, the string must be terminated with two <b>null</b> characters.

<div class="alert"><b>Note</b>  lpData indicating a  <b>null</b> value is valid, however, if this is the case, <i>cbData</i> must be set to '0'.</div>
<div> </div>

### -param cbData [in]

The size of the information pointed to by the <i>lpData</i> parameter, in bytes. If the data is of type REG_SZ, REG_EXPAND_SZ, or REG_MULTI_SZ, <i>cbData</i> must include the size of the terminating <b>null</b> character or characters.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.

## -remarks

Value sizes are limited by available memory. However, storing large values in the registry can affect its performance. Long values (more than 2,048 bytes) should be stored as files, with the locations of the files stored in the registry. 

Application elements such as icons, bitmaps, and executable files should be stored as files and not be placed in the registry.

If <i>dwType</i> is the REG_SZ, REG_MULTI_SZ, or REG_EXPAND_SZ type and the ANSI version of this function is used (either by explicitly calling <b>RegSetValueExA</b> or by not defining UNICODE before including the Windows.h file), the data pointed to by the <i>lpData</i> parameter must be an ANSI character string. The string is converted to Unicode before it is stored in the registry.

Note that operations that access certain registry keys are redirected. For more information,  see <a href="/windows/desktop/SysInfo/registry-virtualization">Registry Virtualization</a> and <a href="/windows/desktop/SysInfo/32-bit-and-64-bit-application-data-in-the-registry">32-bit and 64-bit Application Data in the Registry</a>.

Consider using the <a href="/windows/desktop/api/winreg/nf-winreg-regsetkeyvaluea">RegSetKeyValue</a> function, which provides a more convenient way to set the value of a registry key.

> [!NOTE]
> The winreg.h header defines RegSetValueEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regsetkeyvaluea">RegSetKeyValue</a>

<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>

<a href="/windows/desktop/api/winreg/nf-winreg-regflushkey">RegFlushKey</a>

<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>

<a href="/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa">RegQueryValueEx</a>

<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>

<a href="/windows/desktop/SysInfo/registry">Registry Overview</a>
