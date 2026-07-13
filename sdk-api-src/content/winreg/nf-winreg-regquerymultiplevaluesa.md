---
UID: NF:winreg.RegQueryMultipleValuesA
title: RegQueryMultipleValuesA function (winreg.h)
description: Retrieves the type and data for a list of value names associated with an open registry key. (ANSI)
helpviewer_keywords: ["RegQueryMultipleValuesA", "winreg/RegQueryMultipleValuesA"]
old-location: base\regquerymultiplevalues.htm
tech.root: winprog
ms.assetid: e718534a-6e68-40f5-9cdd-170ce9b5e6e5
ms.date: 12/05/2018
ms.keywords: RegQueryMultipleValues, RegQueryMultipleValues function, RegQueryMultipleValuesA, RegQueryMultipleValuesW, _win32_regquerymultiplevalues, base.regquerymultiplevalues, winreg/RegQueryMultipleValues, winreg/RegQueryMultipleValuesA, winreg/RegQueryMultipleValuesW
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegQueryMultipleValuesW (Unicode) and RegQueryMultipleValuesA (ANSI)
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
 - RegQueryMultipleValuesA
 - winreg/RegQueryMultipleValuesA
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
 - API-MS-Win-Core-Registry-l2-2-0.dll
api_name:
 - RegQueryMultipleValues
 - RegQueryMultipleValuesA
 - RegQueryMultipleValuesW
---

# RegQueryMultipleValuesA function


## -description

Retrieves the type and data for a list of value names associated with an open registry key.

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

### -param val_list [out]

A pointer to an array of 

<a href="/windows/desktop/api/winreg/ns-winreg-valenta">VALENT</a> structures that describe one or more value entries. On input, the <b>ve_valuename</b> member of each structure must contain a pointer to the name of a value to retrieve. The function fails if any of the specified values do not exist in the specified key. 




If the function succeeds, each element of the array contains the information for the specified value.

### -param num_vals [in]

The number of elements in the <i>val_list</i> array.

### -param lpValueBuf [out, optional]

A pointer to a buffer. If the function succeeds, the buffer receives the data for each value. 




If <i>lpValueBuf</i> is <b>NULL</b>, the value pointed to by the <i>ldwTotsize</i> parameter must be zero, in which case the function returns ERROR_MORE_DATA and <i>ldwTotsize</i> receives the required size of the buffer, in bytes.

### -param ldwTotsize [in, out, optional]

A pointer to a variable that specifies the size of the buffer pointed to by the <i>lpValueBuf</i> parameter, in bytes. If the function succeeds, <i>ldwTotsize</i> receives the number of bytes copied to the buffer. If the function fails because the buffer is too small, <i>ldwTotsize</i> receives the required size, in bytes.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANTREAD</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/winreg/nf-winreg-regquerymultiplevaluesa">RegQueryMultipleValues</a> cannot instantiate or access the provider of the dynamic key.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by <i>lpValueBuf</i> was too small. In this case, <i>ldwTotsize</i> receives the required buffer size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_TRANSFER_TOO_LONG</b></dt>
</dl>
</td>
<td width="60%">
The total size of the requested data (size of the <i>val_list</i> array + <i>ldwTotSize</i>) is more than the system limit of one megabyte.

</td>
</tr>
</table>

## -remarks

The 
<b>RegQueryMultipleValues</b> function allows an application to query one or more values of a static or dynamic key. If the target key is a static key, the system provides all of the values in an atomic fashion. To prevent excessive serialization, the aggregate data returned by the function cannot exceed one megabyte.

If the target key is a dynamic key, its provider must provide all the values in an atomic fashion. This means the provider should fill the results buffer synchronously, providing a consistent view of all the values in the buffer while avoiding excessive serialization. The provider can provide at most one megabyte of total output data during an atomic call to this function.

<b>RegQueryMultipleValues</b> is supported remotely; that is, the <i>hKey</i> parameter passed to the function can refer to a remote computer.





> [!NOTE]
> The winreg.h header defines RegQueryMultipleValues as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="/windows/desktop/SysInfo/registry">Registry Overview</a>



<a href="/windows/desktop/api/winreg/ns-winreg-valenta">VALENT</a>
