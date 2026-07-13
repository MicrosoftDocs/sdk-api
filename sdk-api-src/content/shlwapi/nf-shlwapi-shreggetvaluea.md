---
UID: NF:shlwapi.SHRegGetValueA
title: SHRegGetValueA function (shlwapi.h)
description: Retrieves a registry value. (SHRegGetValueA)
helpviewer_keywords: ["HKEY_CLASSES_ROOT", "HKEY_CURRENT_CONFIG", "HKEY_CURRENT_USER", "HKEY_LOCAL_MACHINE", "HKEY_PERFORMANCE_DATA", "HKEY_USERS", "SHRegGetValueA", "shlwapi/SHRegGetValueA"]
old-location: shell\SHRegGetValue.htm
tech.root: shell
ms.assetid: 5650eb4c-40fd-47d7-af76-2688d62d9bca
ms.date: 12/05/2018
ms.keywords: HKEY_CLASSES_ROOT, HKEY_CURRENT_CONFIG, HKEY_CURRENT_USER, HKEY_LOCAL_MACHINE, HKEY_PERFORMANCE_DATA, HKEY_USERS, SHRegGetValue, SHRegGetValue function [Windows Shell], SHRegGetValueA, SHRegGetValueW, _shell_SHRegGetValue, shell.SHRegGetValue, shlwapi/SHRegGetValue, shlwapi/SHRegGetValueA, shlwapi/SHRegGetValueW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHRegGetValueW (Unicode) and SHRegGetValueA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHRegGetValueA
 - shlwapi/SHRegGetValueA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-shlwapi-IE-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-0.dll
 - ShCore.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-1.dll
 - API-MS-Win-ShCore-Registry-l1-1-0.dll
 - API-MS-Win-ShCore-Registry-l1-1-1.dll
api_name:
 - SHRegGetValue
 - SHRegGetValueA
 - SHRegGetValueW
---

# SHRegGetValueA function


## -description

<p class="CCE_Message">[<b>SHRegGetValue</b> may be altered or unavailable in subsequent versions of the operating system or product. Use <a href="/windows/desktop/api/winreg/nf-winreg-reggetvaluea">RegGetValue</a> in its place.]

Retrieves a registry value.

## -parameters

### -param hkey [in]

Type: <b>HKEY</b>

A handle to the currently open key, or any of the following predefined values.

<a id="HKEY_CLASSES_ROOT"></a>
<a id="hkey_classes_root"></a>


#### HKEY_CLASSES_ROOT

<a id="HKEY_CURRENT_CONFIG"></a>
<a id="hkey_current_config"></a>


#### HKEY_CURRENT_CONFIG

<a id="HKEY_CURRENT_USER"></a>
<a id="hkey_current_user"></a>


#### HKEY_CURRENT_USER

<a id="HKEY_LOCAL_MACHINE"></a>
<a id="hkey_local_machine"></a>


#### HKEY_LOCAL_MACHINE

<a id="HKEY_PERFORMANCE_DATA"></a>
<a id="hkey_performance_data"></a>


#### HKEY_PERFORMANCE_DATA

<a id="HKEY_USERS"></a>
<a id="hkey_users"></a>


#### HKEY_USERS

### -param pszSubKey [in]

Type: <b>LPCTSTR</b>

A pointer to a <b>null</b>-terminated string that specifies the relative path from <i>hkey</i> to the subkey to retrieve the value from. This parameter can be <b>NULL</b> or an empty string, in which case the data is retrieved from the <i>hkey</i> location.

### -param pszValue [in]

Type: <b>LPCTSTR</b>

A pointer to a <b>null</b>-terminated string that contains the name of the value. This parameter can be <b>NULL</b> or an empty string, in which case the data is retrieved from the Default value.

### -param srrfFlags [in]

Type: <b><a href="/windows/desktop/shell/srrf">SRRF</a></b>

One or more of the <a href="/windows/desktop/shell/srrf">SRRF</a> flags that restricts the data to be retrieved. At least one type restriction (SRRF_RT) value must be specified.

### -param pdwType [in, out]

Type: <b>LPDWORD</b>

A pointer to a <b>DWORD</b> that receives the type of data stored in the retrieved value. When using default values, the input <i>pdwType</i> is the type of the default value. For possible values, see <a href="/windows/desktop/shell/hkey-type">Registry Data Types</a>. If the SRRF_NOEXPAND flag is not set, REG_EXPAND_SZ types are automatically expanded and returned as REG_SZ. If type information is not required, this parameter can be <b>NULL</b>.

### -param pvData [out]

Type: <b>LPVOID</b>

A pointer to a buffer that receives the value's data. This parameter can be <b>NULL</b> if the data is not needed. For example, if you were testing only for a value's existence, the specific value data would be superfluous.

### -param pcbData [in, out]

Type: <b>LPDWORD</b>

A pointer to a <b>DWORD</b> that, on entry, contains the size of the destination data buffer <i>pvData</i>, in bytes. This value can be <b>NULL</b> only if <i>pvData</i> is <b>NULL</b>. On exit, <i>pcbData</i> points to one of these values.
                    

<table class="clsStd">
<tr>
<th>pvData</th>
<th>Return Value</th>
<th>pcbData</th>
</tr>
<tr>
<td><b>NULL</b></td>
<td>ERROR_SUCCESS</td>
<td>Size in bytes sufficient to hold the registry data. Note that this is not guaranteed to be the precise size, but only a sufficient size.</td>
</tr>
<tr>
<td>Non-<b>NULL</b></td>
<td>ERROR_SUCCESS</td>
<td>Exact number of bytes written to <i>pvData</i>.</td>
</tr>
<tr>
<td>Non-<b>NULL</b></td>
<td>ERROR_MORE_DATA</td>
<td>Size in bytes needed to hold the entire data. Note that this is not guaranteed to be the precise size, but only a sufficient size.</td>
</tr>
</table>

## -returns

Type: <b>LSTATUS</b>

Returns <b>ERROR_SUCCESS</b> if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to retrieve a generic description of the error.

## -remarks

<b>SHRegGetValue</b> provides data type checking, boot mode checking, auto-expansion of REG_EXPAND_SZ data, and guaranteed <b>null</b>-termination of REG_SZ, REG_EXPAND_SZ, and REG_MULTI_SZ data.

The key identified by <i>hkey</i> must have been opened with <a href="/windows/desktop/shell/messages">KEY_QUERY_VALUE</a> security access. If <i>pszSubKey</i> is not <b>NULL</b> or an empty string, that key also must be able to be opened with <b>KEY_QUERY_VALUE</b> security access in the current calling context.

If the data's type is REG_SZ, REG_EXPAND_SZ or REG_MULTI_SZ, then any returned data includes or takes into account the string's <b>null</b>-termination. For example, if <i>pvData</i> is not <b>NULL</b>, the data returned in that buffer is <b>null</b>-terminated. If <i>pcbData</i> is not <b>NULL</b>, the buffer size that it points to includes the bytes required to hold the terminating <b>null</b> character.

Unless the SRRF_NOEXPAND flag is set, string data of type REG_EXPAND_SZ is automatically expanded before being returned. The expanded string's type is reported in <i>pdwType</i> as REG_SZ, the <i>pcbData</i> parameter points to the number of bytes written for the expanded string, and the buffer pointed to by <i>pvData</i> holds the expanded version of the string.

<h3><a id="Performance_Notes"></a><a id="performance_notes"></a><a id="PERFORMANCE_NOTES"></a>Performance Notes</h3>
If <i>pszSubKey</i> is not <b>NULL</b> or an empty string, that key is opened and closed by this function each time it is accessed. If your application must retrieve a series of values from the same subkey, you will see better performance by opening the key using <a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a> before calling <b>SHRegGetValue</b>. Use the key returned in the <i>phkResult</i> parameter of <b>RegOpenKeyEx</b> as the <i>hkey</i> parameter in this function, with <i>pszSubKey</i> set to <b>NULL</b>.

The potential for an additional call to the registry to read or re-read the data exists when the data type is REG_EXPAND_SZ and the SRRF_NOEXPAND flag has not been set. The following conditions result in that additional call.
                    <ul>
<li><i>pvData</i> is <b>NULL</b>, <i>pcbData</i> is not <b>NULL</b>. Though the data is not retrieved, the registry must be read to get the string and that string expanded to determine the required size of the data buffer.</li>
<li><i>pvData</i> is not <b>NULL</b>, but is too small to hold the data. The data is re-read to get the full string, the string is expanded, and the total required size is determined.</li>
</ul>






> [!NOTE]
> The shlwapi.h header defines SHRegGetValue as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa">RegQueryValueEx</a>
