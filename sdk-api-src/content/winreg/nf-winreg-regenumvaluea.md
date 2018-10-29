---
UID: NF:winreg.RegEnumValueA
title: RegEnumValueA function
author: windows-sdk-content
description: Enumerates the values for the specified open registry key. The function copies one indexed value name and data block for the key each time it is called.
old-location: base\regenumvalue.htm
tech.root: sysinfo
ms.assetid: 7014ff96-c655-486f-af32-180b87281b06
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: RegEnumValue, RegEnumValue function, RegEnumValueA, RegEnumValueW, _win32_regenumvalue, base.regenumvalue, winreg/RegEnumValue, winreg/RegEnumValueA, winreg/RegEnumValueW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - RegEnumValue
 - RegEnumValueA
 - RegEnumValueW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegEnumValueA function


## -description


Enumerates the values for the specified open registry key. The function copies one indexed value name and data block for the key each time it is called.


## -parameters




### -param hKey [in]

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
<a href="https://msdn.microsoft.com/a6d3a884-f181-46a5-b655-226c68792e08">Registry Element Size Limits</a>.


### -param lpcchValueName [in, out]

A pointer to a variable that specifies the size of the buffer pointed to by the <i>lpValueName</i> parameter, in characters. When the function returns, the variable receives the number of characters stored in the buffer, not including the terminating <b>null</b> character.

Registry value names are limited to 32,767 bytes. The ANSI version of this function treats this parameter as a <b>SHORT</b> value. Therefore, if you specify a value greater than 32,767 bytes, there is an overflow and the function may return ERROR_MORE_DATA.


### -param lpReserved

This parameter is reserved and must be <b>NULL</b>.


### -param lpType [out, optional]

A pointer to a variable that receives a code indicating the type of data stored in the specified value. For a list of the possible type codes, see 
<a href="https://msdn.microsoft.com/5fd828d6-4d62-4823-a2f1-15782b5cd28c">Registry Value Types</a>. The <i>lpType</i> parameter can be <b>NULL</b> if the type code is not required.


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
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. If there are no more values available, the function returns ERROR_NO_MORE_ITEMS.

If the <i>lpData</i> buffer is too small to receive the value, the function returns ERROR_MORE_DATA.




## -remarks



To enumerate values, an application should initially call the 
<b>RegEnumValue</b> function with the <i>dwIndex</i> parameter set to zero. The application should then increment <i>dwIndex</i> and call the 
<b>RegEnumValue</b> function until there are no more values (until the function returns ERROR_NO_MORE_ITEMS).

The application can also set <i>dwIndex</i> to the index of the last value on the first call to the function and decrement the index until the value with index 0 is enumerated. To retrieve the index of the last value, use the 
<a href="https://msdn.microsoft.com/25eb2cd2-9fdd-4d6f-8071-daab56f9aae1">RegQueryInfoKey</a> function.

While using 
<b>RegEnumValue</b>, an application should not call any registry functions that might change the key being queried.

If the data has the REG_SZ, REG_MULTI_SZ or REG_EXPAND_SZ type, the string may not have been stored with the proper <b>null</b>-terminating characters.  Therefore, even if the function returns ERROR_SUCCESS, the application should ensure that the string is properly terminated before using it; otherwise, it may overwrite a buffer. (Note that REG_MULTI_SZ strings should have two <b>null</b>-terminating characters.)

To determine the maximum size of the name and data buffers, use the 
<a href="https://msdn.microsoft.com/25eb2cd2-9fdd-4d6f-8071-daab56f9aae1">RegQueryInfoKey</a> function.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/3730180a-52bc-4382-83ca-39f162273ba5">Enumerating Registry Subkeys</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a>



<a href="https://msdn.microsoft.com/647d34cc-01ba-4389-be29-b099ed198e7c">RegEnumKeyEx</a>



<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a>



<a href="https://msdn.microsoft.com/25eb2cd2-9fdd-4d6f-8071-daab56f9aae1">RegQueryInfoKey</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/ffb06903-593e-47ce-adb2-baed5d379110">Registry Overview</a>
 

 

