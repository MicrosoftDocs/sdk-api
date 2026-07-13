---
UID: NF:winreg.RegLoadMUIStringA
title: RegLoadMUIStringA function (winreg.h)
description: Loads the specified string from the specified key and subkey. (ANSI)
helpviewer_keywords: ["REG_MUI_STRING_TRUNCATE", "RegLoadMUIStringA", "winreg/RegLoadMUIStringA"]
old-location: base\regloadmuistring.htm
tech.root: winprog
ms.assetid: 76ffc77f-a1bc-4e01-858f-4a76563a2bbc
ms.date: 12/05/2018
ms.keywords: REG_MUI_STRING_TRUNCATE, RegLoadMUIString, RegLoadMUIString function, RegLoadMUIStringA, RegLoadMUIStringW, base.regloadmuistring, winreg/RegLoadMUIString, winreg/RegLoadMUIStringA, winreg/RegLoadMUIStringW
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegLoadMUIStringW (Unicode) and RegLoadMUIStringA (ANSI)
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
 - RegLoadMUIStringA
 - winreg/RegLoadMUIStringA
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
 - RegLoadMUIString
 - RegLoadMUIStringA
 - RegLoadMUIStringW
---

# RegLoadMUIStringA function


## -description

Loads the specified string from the specified key and subkey.

## -parameters

### -param hKey [in]

A handle to an open registry key. The key must have been opened with the KEY_QUERY_VALUE access right. For more information, see 
<a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.

This handle is returned by the 
<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a> or <a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a> function. It can also be one of the following 
<a href="/windows/desktop/SysInfo/predefined-keys">predefined keys</a>:<dl>
<dd><b>HKEY_CLASSES_ROOT</b></dd>
<dd><b>HKEY_CURRENT_CONFIG</b></dd>
<dd><b>HKEY_CURRENT_USER</b></dd>
<dd><b>HKEY_LOCAL_MACHINE</b></dd>
<dd><b>HKEY_USERS</b></dd>
</dl>

### -param pszValue [in, optional]

The name of the registry value.

### -param pszOutBuf [out, optional]

A pointer to a buffer that receives the string.

Strings of the following form receive special handling:

@[<i>path</i>]&#92;<i>dllname</i>,-<i>strID</i>

The string with identifier <i>strID</i> is loaded from <i>dllname</i>; the <i>path</i> is optional. If the <i>pszDirectory</i> parameter is not <b>NULL</b>, the directory is prepended to the path specified in the registry data. Note that <i>dllname</i> can contain environment variables to be expanded.

### -param cbOutBuf [in]

The size of the <i>pszOutBuf</i> buffer, in bytes.

### -param pcbData [out, optional]

A pointer to a variable that receives the size of the data copied to the <i>pszOutBuf</i> buffer, in bytes.

If the buffer is not large enough to hold the data, the function returns ERROR_MORE_DATA and stores the required buffer size in the variable pointed to by <i>pcbData</i>. In this case, the contents of the buffer are undefined.

### -param Flags [in]

This parameter can be 0 or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="REG_MUI_STRING_TRUNCATE"></a><a id="reg_mui_string_truncate"></a><dl>
<dt><b>REG_MUI_STRING_TRUNCATE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The string is truncated to fit the available size of the <i>pszOutBuf</i> buffer. If this flag is specified, <i>pcbData</i> must be <b>NULL</b>.

</td>
</tr>
</table>

### -param pszDirectory [in, optional]

The directory path.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

If the <i>pcbData</i> buffer is too small to receive the string, the function returns ERROR_MORE_DATA.

The ANSI version of this function returns ERROR_CALL_NOT_IMPLEMENTED.

## -remarks

The <b>RegLoadMUIString</b> function is supported only for Unicode. Although both Unicode (W) and ANSI (A) versions of this function are declared, the <b>RegLoadMUIStringA</b> function returns ERROR_CALL_NOT_IMPLEMENTED. Applications should explicitly call <b>RegLoadMUIStringW</b> or specify Unicode as the character set in platform invoke (PInvoke) calls. 

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.





> [!NOTE]
> The winreg.h header defines RegLoadMUIString as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>
