---
UID: NF:winreg.RegSetKeyValueW
title: RegSetKeyValueW function (winreg.h)
description: Sets the data for the specified value in the specified registry key and subkey. (Unicode)
helpviewer_keywords: ["RegSetKeyValue", "RegSetKeyValue function", "RegSetKeyValueW", "base.regsetkeyvalue", "winreg/RegSetKeyValue", "winreg/RegSetKeyValueW"]
old-location: base\regsetkeyvalue.htm
tech.root: winprog
ms.assetid: e27d2dd6-b139-4ac1-8dd8-527022333364
ms.date: 12/05/2018
ms.keywords: RegSetKeyValue, RegSetKeyValue function, RegSetKeyValueA, RegSetKeyValueW, base.regsetkeyvalue, winreg/RegSetKeyValue, winreg/RegSetKeyValueA, winreg/RegSetKeyValueW
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegSetKeyValueW (Unicode) and RegSetKeyValueA (ANSI)
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
 - RegSetKeyValueW
 - winreg/RegSetKeyValueW
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
 - API-MS-Win-Core-Registry-l2-1-0.dll
 - advapi32legacy.dll
 - API-MS-Win-Core-Registry-l1-1-1.dll
 - KernelBase.dll
 - MinKernelBase.dll
api_name:
 - RegSetKeyValue
 - RegSetKeyValueA
 - RegSetKeyValueW
---

# RegSetKeyValueW function


## -description

Sets the data for the specified value in the specified registry key and subkey.

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

### -param lpSubKey [in, optional]

The name of the subkey relative to the key identified by <i>hKey</i>.
If the subkey does not exist, it is created as a non-volatile key with a default security descriptor.
If this parameter is <b>NULL</b>, then the value is created in the key specified by <i>hKey</i>.

### -param lpValueName [in, optional]

The name of the registry value whose data is to be updated.

### -param dwType [in]

The type of data pointed to by the <i>lpData</i> parameter. For a list of the possible types, see 
<a href="/windows/desktop/SysInfo/registry-value-types">Registry Value Types</a>.

### -param lpData [in, optional]

The data to be stored with the specified value name. 

For string-based types, such as REG_SZ, the string must be null-terminated. With the REG_MULTI_SZ data type, the string must be terminated with two null characters.

### -param cbData [in]

The size of the information pointed to by the <i>lpData</i> parameter, in bytes. If the data is of type REG_SZ, REG_EXPAND_SZ, or REG_MULTI_SZ, <i>cbData</i> must include the size of the terminating null character or characters.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.

## -remarks

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.





> [!NOTE]
> The winreg.h header defines RegSetKeyValue as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regdeletekeyvaluea">RegDeleteKeyValue</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>
