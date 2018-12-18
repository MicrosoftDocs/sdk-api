---
UID: NF:winreg.RegGetValueA
title: RegGetValueA function
author: windows-sdk-content
description: Retrieves the type and data for the specified registry value.
old-location: base\reggetvalue.htm
tech.root: sysinfo
ms.assetid: 1c06facb-6735-4b3f-b77d-f162e3faaada
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RRF_NOEXPAND, RRF_RT_ANY, RRF_RT_DWORD, RRF_RT_QWORD, RRF_RT_REG_BINARY, RRF_RT_REG_DWORD, RRF_RT_REG_EXPAND_SZ, RRF_RT_REG_MULTI_SZ, RRF_RT_REG_NONE, RRF_RT_REG_QWORD, RRF_RT_REG_SZ, RRF_SUBKEY_WOW6432KEY, RRF_SUBKEY_WOW6464KEY, RRF_ZEROONFAILURE, RegGetValue, RegGetValue function, RegGetValueA, RegGetValueW, base.reggetvalue, winreg/RegGetValue, winreg/RegGetValueA, winreg/RegGetValueW
ms.topic: function
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP Professional x64 Edition [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegGetValueW (Unicode) and RegGetValueA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Core-Localregistry-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Registry-l1-1-0.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - MinKernelBase.dll
 - api-ms-win-core-registry-l1-1-1.dll
api_name:
 - RegGetValue
 - RegGetValueA
 - RegGetValueW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegGetValueA function


## -description


Retrieves the type and data for the specified registry value.


## -parameters




### -param hkey [in]

A handle to an open registry key. The key must have been opened with the KEY_QUERY_VALUE access right. For more information, see 
<a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>. 




This handle is returned by the 
<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a>, <a href="https://msdn.microsoft.com/f18e5ff9-41c3-4c26-8d01-a8ec69bcdef2">RegCreateKeyTransacted</a>, <a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a>, or 
<a href="https://msdn.microsoft.com/11663ed2-d17c-4f08-be7b-9b591271fbcd">RegOpenKeyTransacted</a> function. It can also be one of the following 
<a href="https://msdn.microsoft.com/db747656-b414-4594-ad39-6b476799060c">predefined keys</a>:<dl>
<dd><b>HKEY_CLASSES_ROOT</b></dd>
<dd><b>HKEY_CURRENT_CONFIG</b></dd>
<dd><b>HKEY_CURRENT_USER</b></dd>
<dd><b>HKEY_LOCAL_MACHINE</b></dd>
<dd><b>HKEY_PERFORMANCE_DATA</b></dd>
<dd><b>HKEY_PERFORMANCE_NLSTEXT</b></dd>
<dd><b>HKEY_PERFORMANCE_TEXT</b></dd>
<dd><b>HKEY_USERS</b></dd>
</dl>



### -param lpSubKey [in, optional]

The name of the registry key. This key must be a subkey of the key specified by the <i>hkey</i> parameter.

Key names are not case sensitive.


### -param lpValue [in, optional]

The name of the registry value. 




If this parameter is <b>NULL</b> or an empty string, "", the function retrieves the type and data for the key's unnamed or default value, if any.

For more information, see 
<a href="https://msdn.microsoft.com/a6d3a884-f181-46a5-b655-226c68792e08">Registry Element Size Limits</a>.

Keys do not automatically have an unnamed or default value. Unnamed values can be of any type.


### -param dwFlags [in, optional]

The flags that restrict the data type of value to be queried. If the data type of the value does not meet this criteria, the function fails. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RRF_RT_ANY"></a><a id="rrf_rt_any"></a><dl>
<dt><b>RRF_RT_ANY</b></dt>
<dt>0x0000ffff</dt>
</dl>
</td>
<td width="60%">
No type restriction.

</td>
</tr>
<tr>
<td width="40%"><a id="RRF_RT_DWORD"></a><a id="rrf_rt_dword"></a><dl>
<dt><b>RRF_RT_DWORD</b></dt>
<dt>0x00000018</dt>
</dl>
</td>
<td width="60%">
Restrict type to 32-bit RRF_RT_REG_BINARY | RRF_RT_REG_DWORD.

</td>
</tr>
<tr>
<td width="40%"><a id="RRF_RT_QWORD"></a><a id="rrf_rt_qword"></a><dl>
<dt><b>RRF_RT_QWORD</b></dt>
<dt>0x00000048</dt>
</dl>
</td>
<td width="60%">
Restrict type to 64-bit RRF_RT_REG_BINARY | RRF_RT_REG_DWORD.

</td>
</tr>
<tr>
<td width="40%"><a id="RRF_RT_REG_BINARY"></a><a id="rrf_rt_reg_binary"></a><dl>
<dt><b>RRF_RT_REG_BINARY</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Restrict type to REG_BINARY.

</td>
</tr>
<tr>
<td width="40%"><a id="RRF_RT_REG_DWORD"></a><a id="rrf_rt_reg_dword"></a><dl>
<dt><b>RRF_RT_REG_DWORD</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Restrict type to REG_DWORD.

</td>
</tr>
<tr>
<td width="40%"><a id="RRF_RT_REG_EXPAND_SZ"></a><a id="rrf_rt_reg_expand_sz"></a><dl>
<dt><b>RRF_RT_REG_EXPAND_SZ</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Restrict type to REG_EXPAND_SZ.

</td>
</tr>
<tr>
<td width="40%"><a id="RRF_RT_REG_MULTI_SZ"></a><a id="rrf_rt_reg_multi_sz"></a><dl>
<dt><b>RRF_RT_REG_MULTI_SZ</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Restrict type to REG_MULTI_SZ.

</td>
</tr>
<tr>
<td width="40%"><a id="RRF_RT_REG_NONE"></a><a id="rrf_rt_reg_none"></a><dl>
<dt><b>RRF_RT_REG_NONE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Restrict type to REG_NONE.

</td>
</tr>
<tr>
<td width="40%"><a id="RRF_RT_REG_QWORD"></a><a id="rrf_rt_reg_qword"></a><dl>
<dt><b>RRF_RT_REG_QWORD</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Restrict type to REG_QWORD.

</td>
</tr>
<tr>
<td width="40%"><a id="RRF_RT_REG_SZ"></a><a id="rrf_rt_reg_sz"></a><dl>
<dt><b>RRF_RT_REG_SZ</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Restrict type to REG_SZ.

</td>
</tr>
</table>
 


This parameter can also include one or more of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RRF_NOEXPAND"></a><a id="rrf_noexpand"></a><dl>
<dt><b>RRF_NOEXPAND</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
Do not automatically expand environment strings if the value is of type REG_EXPAND_SZ.

</td>
</tr>
<tr>
<td width="40%"><a id="RRF_ZEROONFAILURE"></a><a id="rrf_zeroonfailure"></a><dl>
<dt><b>RRF_ZEROONFAILURE</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
If <i>pvData</i> is not <b>NULL</b>, set the contents of the buffer to zeroes on failure.

</td>
</tr>
<tr>
<td width="40%"><a id="RRF_SUBKEY_WOW6464KEY"></a><a id="rrf_subkey_wow6464key"></a><dl>
<dt><b>RRF_SUBKEY_WOW6464KEY</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
If <i>lpSubKey</i> is not <b>NULL</b>, open the subkey that  <i>lpSubKey</i> specifies with the KEY_WOW64_64KEY access rights.
 For information about these access rights, see <a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>.

You cannot specify <b>RRF_SUBKEY_WOW6464KEY</b> in combination with  <b>RRF_SUBKEY_WOW6432KEY</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="RRF_SUBKEY_WOW6432KEY"></a><a id="rrf_subkey_wow6432key"></a><dl>
<dt><b>RRF_SUBKEY_WOW6432KEY</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
If <i>lpSubKey</i> is not <b>NULL</b>, open the subkey that  <i>lpSubKey</i> specifies with the KEY_WOW64_32KEY access rights.
For information about these access rights, see <a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>.

You cannot specify <b>RRF_SUBKEY_WOW6432KEY</b> in combination with  <b>RRF_SUBKEY_WOW6464KEY</b>.

</td>
</tr>
</table>
 


### -param pdwType [out, optional]

A pointer to a variable that receives a code indicating the type of data stored in the specified value. For a list of the possible type codes, see 
<a href="https://msdn.microsoft.com/5fd828d6-4d62-4823-a2f1-15782b5cd28c">Registry Value Types</a>. This parameter can be <b>NULL</b> if the type is not required.


### -param pvData [out, optional]

A pointer to a buffer that receives the value's data. This parameter can be <b>NULL</b> if the data is not required.

If the data is a string, the function checks for a terminating <b>null</b> character. If one is not found, the string is stored with a <b>null</b> terminator if the buffer is large enough to accommodate the extra character. Otherwise, the function fails and returns ERROR_MORE_DATA.


### -param pcbData [in, out, optional]

A pointer to a variable that specifies the size of the buffer pointed to by the <i>pvData</i> parameter, in bytes. When the function returns, this variable contains the size of the data copied to <i>pvData</i>. 




The <i>pcbData</i> parameter can be <b>NULL</b> only if <i>pvData</i> is <b>NULL</b>.

If the data has the REG_SZ, REG_MULTI_SZ or REG_EXPAND_SZ type, this size includes any terminating <b>null</b> character or characters. For more information, see Remarks.

If the buffer specified by <i>pvData</i> parameter is not large enough to hold the data, the function returns ERROR_MORE_DATA and stores the required buffer size in the variable pointed to by <i>pcbData</i>. In this case, the contents of the <i>pvData</i> buffer are undefined.

If <i>pvData</i> is <b>NULL</b>, and <i>pcbData</i> is non-<b>NULL</b>, the function returns ERROR_SUCCESS and stores the size of the data, in bytes, in the variable pointed to by <i>pcbData</i>. This enables an application to determine the best way to allocate a buffer for the value's data.

If <i>hKey</i> specifies <b>HKEY_PERFORMANCE_DATA</b> and the <i>pvData</i> buffer is not large enough to contain all of the returned data, 
the function returns ERROR_MORE_DATA and the value returned through the <i>pcbData</i> parameter is undefined. This is because the size of the performance data can change from one call to the next. In this case, you must increase the buffer size and call 
<b>RegGetValue</b> again passing the updated buffer size in the <i>pcbData</i> parameter. Repeat this until the function succeeds. You need to maintain a separate variable to keep track of the buffer size, because the value returned by <i>pcbData</i> is unpredictable.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.

If the <i>pvData</i> buffer is too small to receive the value, the function returns ERROR_MORE_DATA.

If <i>dwFlags</i> specifies a combination of both <b>RRF_SUBKEY_WOW6464KEY</b> and  <b>RRF_SUBKEY_WOW6432KEY</b>, the function returns ERROR_INVALID_PARAMETER.




## -remarks



An application typically calls <a href="https://msdn.microsoft.com/7014ff96-c655-486f-af32-180b87281b06">RegEnumValue</a> to determine the value names and then <b>RegGetValue</b> to retrieve the data for the names.

If the data has the REG_SZ, REG_MULTI_SZ or REG_EXPAND_SZ type, and the ANSI version of this function is used (either by explicitly calling <b>RegGetValueA</b> or by not defining UNICODE before including the Windows.h file), this function converts the stored Unicode string to an ANSI string before copying it to the buffer pointed to by <i>pvData</i>.

When calling this function with <i>hkey</i> set to the <b>HKEY_PERFORMANCE_DATA</b> handle and a value string of a specified object, the returned data structure sometimes has unrequested objects. Do not be surprised; this is normal behavior. You should always expect to walk the returned data structure to look for the requested object.

Note that operations that access certain registry keys are redirected. For more information,  see <a href="https://msdn.microsoft.com/dace2f65-df60-419a-8be8-ab60668e6396">Registry Virtualization</a> and <a href="https://msdn.microsoft.com/08dc034c-15ce-41d9-8e74-a49b61ad40a6">32-bit and 64-bit Application Data in the Registry</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a>



<a href="https://msdn.microsoft.com/647d34cc-01ba-4389-be29-b099ed198e7c">RegEnumKeyEx</a>



<a href="https://msdn.microsoft.com/7014ff96-c655-486f-af32-180b87281b06">RegEnumValue</a>



<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a>



<a href="https://msdn.microsoft.com/25eb2cd2-9fdd-4d6f-8071-daab56f9aae1">RegQueryInfoKey</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/ffb06903-593e-47ce-adb2-baed5d379110">Registry Overview</a>
 

 

