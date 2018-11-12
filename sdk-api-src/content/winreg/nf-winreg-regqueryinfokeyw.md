---
UID: NF:winreg.RegQueryInfoKeyW
title: RegQueryInfoKeyW function
author: windows-sdk-content
description: Retrieves information about the specified registry key.
old-location: base\regqueryinfokey.htm
tech.root: sysinfo
ms.assetid: 25eb2cd2-9fdd-4d6f-8071-daab56f9aae1
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: RegQueryInfoKey, RegQueryInfoKey function, RegQueryInfoKeyA, RegQueryInfoKeyW, _win32_regqueryinfokey, base.regqueryinfokey, winreg/RegQueryInfoKey, winreg/RegQueryInfoKeyA, winreg/RegQueryInfoKeyW
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
req.unicode-ansi: RegQueryInfoKeyW (Unicode) and RegQueryInfoKeyA (ANSI)
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
 - RegQueryInfoKey
 - RegQueryInfoKeyA
 - RegQueryInfoKeyW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegQueryInfoKeyW function


## -description


Retrieves information about the specified registry key.


## -parameters




### -param hKey [in]

A handle to an open registry key. The key must have been opened with the KEY_QUERY_VALUE access right. For more information, see 
<a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>. 




This handle is returned by the 
<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a>, <a href="https://msdn.microsoft.com/f18e5ff9-41c3-4c26-8d01-a8ec69bcdef2">RegCreateKeyTransacted</a>, <a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a>, or 
<a href="https://msdn.microsoft.com/11663ed2-d17c-4f08-be7b-9b591271fbcd">RegOpenKeyTransacted</a> function. It can also be one of the following 
<a href="https://msdn.microsoft.com/db747656-b414-4594-ad39-6b476799060c">predefined keys</a>:<pre xml:space="preserve"><b></b>
   <b>HKEY_CLASSES_ROOT</b>
   <b>HKEY_CURRENT_CONFIG</b>
   <b>HKEY_CURRENT_USER</b>
   <b>HKEY_LOCAL_MACHINE</b>
   <b>HKEY_PERFORMANCE_DATA</b>
   <b>HKEY_USERS</b></pre>



### -param lpClass [out, optional]

A pointer to a buffer that receives the user-defined class of the key. This parameter can be <b>NULL</b>.


### -param lpcchClass [in, out, optional]

A pointer to a variable that specifies the size of the buffer pointed to by the <i>lpClass</i> parameter, in characters. 

The size should include the terminating <b>null</b> character. When the function returns, this variable contains the size of the class string that is stored in the buffer. The count returned does not include the terminating <b>null</b> character. If the buffer is not big enough, the function returns ERROR_MORE_DATA, and the variable contains the size of the string, in characters, without counting the terminating <b>null</b> character.

If <i>lpClass</i> is <b>NULL</b>, <i>lpcClass</i> can be <b>NULL</b>.

If the <i>lpClass</i> parameter is a valid address, but the <i>lpcClass</i> parameter is not, for example, it is <b>NULL</b>, then the  function returns ERROR_INVALID_PARAMETER.


### -param lpReserved

This parameter is reserved and must be <b>NULL</b>.


### -param lpcSubKeys [out, optional]

A pointer to a variable that receives the number of subkeys that are contained by the specified key. This parameter can be <b>NULL</b>.


### -param lpcbMaxSubKeyLen [out, optional]

A pointer to a variable that receives the size of the key's subkey with the longest name, in Unicode characters, not including the terminating <b>null</b> character. This parameter can be <b>NULL</b>. 



					


### -param lpcbMaxClassLen [out, optional]

A pointer to a variable that receives the size of the longest string that specifies a subkey class, in Unicode characters. The count returned does not include the terminating <b>null</b> character. This parameter can be <b>NULL</b>.


### -param lpcValues [out, optional]

A pointer to a variable that receives the number of values that are associated with the key. This parameter can be <b>NULL</b>.


### -param lpcbMaxValueNameLen [out, optional]

A pointer to a variable that receives the size of the key's longest value name, in Unicode characters. The size does not include the terminating <b>null</b> character. This parameter can be <b>NULL</b>.


### -param lpcbMaxValueLen [out, optional]

A pointer to a variable that receives the size of the longest data component among the key's values, in bytes. This parameter can be <b>NULL</b>.


### -param lpcbSecurityDescriptor [out, optional]

A pointer to a variable that receives the size of the key's security descriptor, in bytes. This parameter can be <b>NULL</b>.


### -param lpftLastWriteTime [out, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that receives the last write time. This parameter can be <b>NULL</b>. 




The function sets the members of the 
<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure to indicate the last time that the key or any of its value entries is modified.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.

If the <i>lpClass</i> buffer is too small to receive the name of the class, the function returns ERROR_MORE_DATA.




## -see-also




<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>



<a href="https://msdn.microsoft.com/a2310ca0-1b9f-48d1-a3b5-ea3a528bfaba">RegDeleteKey</a>



<a href="https://msdn.microsoft.com/647d34cc-01ba-4389-be29-b099ed198e7c">RegEnumKeyEx</a>



<a href="https://msdn.microsoft.com/7014ff96-c655-486f-af32-180b87281b06">RegEnumValue</a>



<a href="https://msdn.microsoft.com/202d253a-10ff-40e7-8eec-a49717443b81">RegQueryValueEx</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/ffb06903-593e-47ce-adb2-baed5d379110">Registry Overview</a>
 

 

