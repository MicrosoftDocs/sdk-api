---
UID: NF:winreg.RegEnumKeyA
title: RegEnumKeyA function
author: windows-sdk-content
description: Enumerates the subkeys of the specified open registry key.
old-location: base\regenumkey.htm
old-project: sysinfo
ms.assetid: 18a05c60-6c6d-438f-9003-f07d688d86a3
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: RegEnumKey, RegEnumKey function, RegEnumKeyA, RegEnumKeyW, _win32_regenumkey, base.regenumkey, winreg/RegEnumKey, winreg/RegEnumKeyA, winreg/RegEnumKeyW
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
req.unicode-ansi: RegEnumKeyW (Unicode) and RegEnumKeyA (ANSI)
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
 - API-MS-Win-Core-Registry-l2-1-0.dll
 - advapi32legacy.dll
 - API-MS-Win-Core-Registry-l2-2-0.dll
api_name:
 - RegEnumKey
 - RegEnumKeyA
 - RegEnumKeyW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RegEnumKeyA function


## -description


Enumerates the subkeys of the specified open registry key. The function retrieves the name of one subkey each time it is called.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should use the 
<a href="https://msdn.microsoft.com/647d34cc-01ba-4389-be29-b099ed198e7c">RegEnumKeyEx</a> function.</div><div> </div>

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
<dd><b>HKEY_USERS</b></dd>
</dl>



### -param dwIndex [in]

The index of the subkey of <i>hKey</i> to be retrieved. This value should be zero for the first call to the 
<b>RegEnumKey</b> function and then incremented for subsequent calls. 




Because subkeys are not ordered, any new subkey will have an arbitrary index. This means that the function may return subkeys in any order.


### -param lpName [out]

A pointer to a buffer that receives the name of the subkey, including the terminating null character. This function copies only the name of the subkey, not the full key hierarchy, to the buffer. 




For more information, see 
<a href="https://msdn.microsoft.com/a6d3a884-f181-46a5-b655-226c68792e08">Registry Element Size Limits</a>.


### -param cchName [in]

The size of the buffer pointed to by the <i>lpName</i> parameter, in <b>TCHARs</b>. To determine the required buffer size, use the 
<a href="https://msdn.microsoft.com/25eb2cd2-9fdd-4d6f-8071-daab56f9aae1">RegQueryInfoKey</a> function to determine the size of the largest subkey for the key identified by the <i>hKey</i> parameter.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. If there are no more subkeys available, the function returns ERROR_NO_MORE_ITEMS.

If the <i>lpName</i> buffer is too small to receive the name of the key, the function returns ERROR_MORE_DATA.




## -remarks



To enumerate subkeys, an application should initially call the 
<b>RegEnumKey</b> function with the <i>dwIndex</i> parameter set to zero. The application should then increment the <i>dwIndex</i> parameter and call the 
<b>RegEnumKey</b> function until there are no more subkeys (meaning the function returns ERROR_NO_MORE_ITEMS).

The application can also set <i>dwIndex</i> to the index of the last key on the first call to the function and decrement the index until the subkey with index 0 is enumerated. To retrieve the index of the last subkey, use the 
<a href="https://msdn.microsoft.com/25eb2cd2-9fdd-4d6f-8071-daab56f9aae1">RegQueryInfoKey</a>.

While an application is using the 
<b>RegEnumKey</b> function, it should not make calls to any registration functions that might change the key being queried.




## -see-also




<a href="https://msdn.microsoft.com/10175499-abf3-4694-9594-bb97b43f3fa5">RegCloseKey</a>



<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a>



<a href="https://msdn.microsoft.com/a2310ca0-1b9f-48d1-a3b5-ea3a528bfaba">RegDeleteKey</a>



<a href="https://msdn.microsoft.com/647d34cc-01ba-4389-be29-b099ed198e7c">RegEnumKeyEx</a>



<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a>



<a href="https://msdn.microsoft.com/25eb2cd2-9fdd-4d6f-8071-daab56f9aae1">RegQueryInfoKey</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/ffb06903-593e-47ce-adb2-baed5d379110">Registry Overview</a>
 

 

