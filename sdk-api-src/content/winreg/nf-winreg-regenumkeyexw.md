---
UID: NF:winreg.RegEnumKeyExW
title: RegEnumKeyExW function
author: windows-sdk-content
description: Enumerates the subkeys of the specified open registry key. The function retrieves information about one subkey each time it is called.
old-location: base\regenumkeyex.htm
old-project: SysInfo
ms.assetid: 647d34cc-01ba-4389-be29-b099ed198e7c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RegEnumKeyEx, RegEnumKeyEx function, RegEnumKeyExA, RegEnumKeyExW, _win32_regenumkeyex, base.regenumkeyex, winreg/RegEnumKeyEx, winreg/RegEnumKeyExA, winreg/RegEnumKeyExW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winreg.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegEnumKeyExW (Unicode) and RegEnumKeyExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PERF_OBJECT_TYPE, *PPERF_OBJECT_TYPE
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
 - RegEnumKeyEx
 - RegEnumKeyExA
 - RegEnumKeyExW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RegEnumKeyExW function


## -description


Enumerates the subkeys of the specified open registry key. The function retrieves information about one subkey each time it is called.


## -parameters




### -param hKey [in]

A handle to an open registry key. The key must have been opened with the KEY_ENUMERATE_SUB_KEYS access right. For more information, see 
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

The index of the subkey to retrieve. This parameter should be zero for the first call to the 
<b>RegEnumKeyEx</b> function and then incremented for subsequent calls. 




Because subkeys are not ordered, any new subkey will have an arbitrary index. This means that the function may return subkeys in any order.


### -param lpName [out]

A pointer to a buffer that receives the name of the subkey, including the terminating <b>null</b> character. The function copies only the name of the subkey, not the full key hierarchy, to the buffer. 


If the function fails, no information is copied to this buffer.

For more information, see 
<a href="https://msdn.microsoft.com/a6d3a884-f181-46a5-b655-226c68792e08">Registry Element Size Limits</a>.


### -param lpcchName [in, out]

A pointer to a variable that specifies the size of the buffer specified by the <i>lpName</i> parameter, in characters. This size should include the terminating <b>null</b> character. If the function succeeds, the variable pointed to by <i>lpcName</i> contains the number of characters stored in the buffer, not including the terminating <b>null</b> character.

To determine the required buffer size, use the 
<a href="https://msdn.microsoft.com/25eb2cd2-9fdd-4d6f-8071-daab56f9aae1">RegQueryInfoKey</a> function to determine the size of the largest subkey for the key identified by the <i>hKey</i> parameter.


### -param lpReserved

This parameter is reserved and must be <b>NULL</b>.


### -param lpClass [in, out]

A pointer to a buffer that receives the user-defined class of the enumerated subkey. This parameter can be <b>NULL</b>.


### -param lpcchClass [in, out, optional]

A pointer to a variable that specifies the size of the buffer specified by the <i>lpClass</i> parameter, in characters. The size should include the terminating <b>null</b> character. If the function succeeds, <i>lpcClass</i> contains the number of characters stored in the buffer, not including the terminating <b>null</b> character. This parameter can be <b>NULL</b> only if <i>lpClass</i> is <b>NULL</b>.


### -param lpftLastWriteTime [out, optional]

A pointer to <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that receives the time at which the enumerated subkey was last written. This parameter can be <b>NULL</b>.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. If there are no more subkeys available, the function returns ERROR_NO_MORE_ITEMS.

If the <i>lpName</i> buffer is too small to receive the name of the key, the function returns ERROR_MORE_DATA.




## -remarks



To enumerate subkeys, an application should initially call the 
<b>RegEnumKeyEx</b> function with the <i>dwIndex</i> parameter set to zero. The application should then increment the <i>dwIndex</i> parameter and call 
<b>RegEnumKeyEx</b> until there are no more subkeys (meaning the function returns ERROR_NO_MORE_ITEMS).

The application can also set <i>dwIndex</i> to the index of the last subkey on the first call to the function and decrement the index until the subkey with the index 0 is enumerated. To retrieve the index of the last subkey, use the 
<a href="https://msdn.microsoft.com/25eb2cd2-9fdd-4d6f-8071-daab56f9aae1">RegQueryInfoKey</a> function.

While an application is using the 
<b>RegEnumKeyEx</b> function, it should not make calls to any registration functions that might change the key being enumerated.

Note that operations that access certain registry keys are redirected. For more information,  see <a href="https://msdn.microsoft.com/dace2f65-df60-419a-8be8-ab60668e6396">Registry Virtualization</a> and <a href="https://msdn.microsoft.com/08dc034c-15ce-41d9-8e74-a49b61ad40a6">32-bit and 64-bit Application Data in the Registry</a>.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/3730180a-52bc-4382-83ca-39f162273ba5">Enumerating Registry Subkeys</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>



<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a>



<a href="https://msdn.microsoft.com/a2310ca0-1b9f-48d1-a3b5-ea3a528bfaba">RegDeleteKey</a>



<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a>



<a href="https://msdn.microsoft.com/25eb2cd2-9fdd-4d6f-8071-daab56f9aae1">RegQueryInfoKey</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/ffb06903-593e-47ce-adb2-baed5d379110">Registry Overview</a>
 

 

