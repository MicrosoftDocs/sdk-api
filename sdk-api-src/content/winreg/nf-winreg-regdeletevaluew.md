---
UID: NF:winreg.RegDeleteValueW
title: RegDeleteValueW function (winreg.h)
description: Removes a named value from the specified registry key. (Unicode)
helpviewer_keywords: ["RegDeleteValue", "RegDeleteValue function", "RegDeleteValueW", "_win32_regdeletevalue", "base.regdeletevalue", "winreg/RegDeleteValue", "winreg/RegDeleteValueW"]
old-location: base\regdeletevalue.htm
tech.root: winprog
ms.assetid: 4393b4ef-cd10-40d4-bb12-2d84e7cb7d3c
ms.date: 12/05/2018
ms.keywords: RegDeleteValue, RegDeleteValue function, RegDeleteValueA, RegDeleteValueW, _win32_regdeletevalue, base.regdeletevalue, winreg/RegDeleteValue, winreg/RegDeleteValueA, winreg/RegDeleteValueW
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegDeleteValueW (Unicode) and RegDeleteValueA (ANSI)
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
 - RegDeleteValueW
 - winreg/RegDeleteValueW
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
 - RegDeleteValue
 - RegDeleteValueA
 - RegDeleteValueW
---

# RegDeleteValueW function


## -description

Removes a named value from the specified registry key. Note that value names are not case sensitive.

## -parameters

### -param hKey [in]

A handle to an open registry key. The key must have been opened with the KEY_SET_VALUE access right. For more information, see 
<a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>. 




This handle is returned by the 
<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>, <a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeytransacteda">RegCreateKeyTransacted</a>, <a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>, or 
<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeytransacteda">RegOpenKeyTransacted</a> function. It can also be one of the following 
<a href="/windows/desktop/SysInfo/predefined-keys">predefined keys</a>:


<pre><b></b>
   <b>HKEY_CLASSES_ROOT</b>
   <b>HKEY_CURRENT_CONFIG</b>
   <b>HKEY_CURRENT_USER</b>
   <b>HKEY_LOCAL_MACHINE</b>
   <b>HKEY_USERS</b></pre>

### -param lpValueName [in, optional]

The registry value to be removed. If this parameter is <b>NULL</b> or an empty string, the value set by the 
<a href="/windows/desktop/api/winreg/nf-winreg-regsetvaluea">RegSetValue</a> function is removed. 




For more information, see 
<a href="/windows/desktop/SysInfo/registry-element-size-limits">Registry Element Size Limits</a>.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regsetvalueexa">RegSetValueEx</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="/windows/desktop/SysInfo/registry">Registry Overview</a>

## -remarks

> [!NOTE]
> The winreg.h header defines RegDeleteValue as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
