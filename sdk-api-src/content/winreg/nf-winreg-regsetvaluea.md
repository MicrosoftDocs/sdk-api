---
UID: NF:winreg.RegSetValueA
title: RegSetValueA function (winreg.h)
description: Sets the data for the default or unnamed value of a specified registry key. The data must be a text string. (ANSI)
helpviewer_keywords: ["RegSetValueA", "winreg/RegSetValueA"]
old-location: base\regsetvalue.htm
tech.root: winprog
ms.assetid: f99774d4-575b-43a3-8887-e15acb0477fd
ms.date: 12/05/2018
ms.keywords: RegSetValue, RegSetValue function, RegSetValueA, RegSetValueW, _win32_regsetvalue, base.regsetvalue, winreg/RegSetValue, winreg/RegSetValueA, winreg/RegSetValueW
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegSetValueW (Unicode) and RegSetValueA (ANSI)
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
 - RegSetValueA
 - winreg/RegSetValueA
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
 - RegSetValue
 - RegSetValueA
 - RegSetValueW
---

# RegSetValueA function


## -description

Sets the data for the default or unnamed value of a specified registry key. The data must be a text string.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should use the 
<a href="/windows/desktop/api/winreg/nf-winreg-regsetvalueexa">RegSetValueEx</a> function.</div><div> </div>

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
</dl>

### -param lpSubKey [in, optional]

The name of a subkey of the <i>hKey</i> parameter. The function sets the default value of the specified subkey. If <i>lpSubKey</i> does not exist, the function creates it.

Key names are not case sensitive.

If this parameter is <b>NULL</b> or points to an empty string, the function sets the default value of the key identified by <i>hKey</i>.

For more information, see 
<a href="/windows/desktop/SysInfo/registry-element-size-limits">Registry Element Size Limits</a>.

### -param dwType [in]

The type of information to be stored. This parameter must be the REG_SZ type. To store other data types, use the 
<a href="/windows/desktop/api/winreg/nf-winreg-regsetvalueexa">RegSetValueEx</a> function.

### -param lpData [in]

The data to be stored. This parameter cannot be <b>NULL</b>.

### -param cbData [in]

This parameter is ignored. The function calculates this value based on the size of the data in the <i>lpData</i> parameter.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.

## -remarks

If the key specified by the <i>lpSubKey</i> parameter does not exist, the 
<b>RegSetValue</b> function creates it.

If the ANSI version of this function is used (either by explicitly calling <b>RegSetValueA</b> or by not defining UNICODE before including the Windows.h file), the <i>lpData</i> parameter must be an ANSI character string. The string is converted to Unicode before it is stored in the registry.





> [!NOTE]
> The winreg.h header defines RegSetValue as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regflushkey">RegFlushKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa">RegQueryValueEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regsetvalueexa">RegSetValueEx</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="/windows/desktop/SysInfo/registry">Registry Overview</a>
