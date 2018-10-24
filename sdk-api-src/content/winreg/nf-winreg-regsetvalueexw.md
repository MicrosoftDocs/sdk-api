---
UID: NF:winreg.RegSetValueExW
title: RegSetValueExW function
author: windows-sdk-content
description: Sets the data and type of a specified value under a registry key.
old-location: base\regsetvalueex.htm
tech.root: sysinfo
ms.assetid: 29b0e27c-4999-4e92-bd8b-bba74920bccc
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: RegSetValueEx, RegSetValueEx function, RegSetValueExA, RegSetValueExW, _win32_regsetvalueex, base.regsetvalueex, winreg/RegSetValueEx, winreg/RegSetValueExA, winreg/RegSetValueExW
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
req.unicode-ansi: RegSetValueExW (Unicode) and RegSetValueExA (ANSI)
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
 - RegSetValueEx
 - RegSetValueExA
 - RegSetValueExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegSetValueExW function


## -description


Sets the data and type of a specified value under a registry key.


## -parameters




### -param hKey [in]

A handle to an open registry key. The key must have been opened with the KEY_SET_VALUE access right. For more information, see 
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
</dl>The Unicode version of this function supports the following additional predefined keys:<ul>
<li><b>HKEY_PERFORMANCE_TEXT</b></li>
<li><b>HKEY_PERFORMANCE_NLSTEXT</b></li>
</ul>



### -param lpValueName [in, optional]

The name of the value to be set. If a value with this name is not already present in the key, the function adds it to the key. 




If <i>lpValueName</i> is <b>NULL</b> or an empty string, "", the function sets the type and data for the key's unnamed or default value.

For more information, see 
<a href="https://msdn.microsoft.com/a6d3a884-f181-46a5-b655-226c68792e08">Registry Element Size Limits</a>.

Registry keys do not have default values, but they can have one unnamed value, which can be of any type.


### -param Reserved

This parameter is reserved and must be zero.


### -param dwType [in]

The type of data pointed to by the <i>lpData</i> parameter. For a list of the possible types, see 
<a href="https://msdn.microsoft.com/5fd828d6-4d62-4823-a2f1-15782b5cd28c">Registry Value Types</a>.


### -param lpData [in]

The data to be stored. 

For string-based types, such as REG_SZ, the string must be <b>null</b>-terminated. With the REG_MULTI_SZ data type, the string must be terminated with two <b>null</b> characters.

<div class="alert"><b>Note</b>  lpData indicating a  <b>null</b> value is valid, however, if this is the case, <i>cbData</i> must be set to '0'.</div>
<div> </div>

### -param cbData [in]

The size of the information pointed to by the <i>lpData</i> parameter, in bytes. If the data is of type REG_SZ, REG_EXPAND_SZ, or REG_MULTI_SZ, <i>cbData</i> must include the size of the terminating <b>null</b> character or characters.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



Value sizes are limited by available memory. However, storing large values in the registry can affect its performance. Long values (more than 2,048 bytes) should be stored as files, with the locations of the files stored in the registry. 

Application elements such as icons, bitmaps, and executable files should be stored as files and not be placed in the registry.

If <i>dwType</i> is the REG_SZ, REG_MULTI_SZ, or REG_EXPAND_SZ type and the ANSI version of this function is used (either by explicitly calling <b>RegSetValueExA</b> or by not defining UNICODE before including the Windows.h file), the data pointed to by the <i>lpData</i> parameter must be an ANSI character string. The string is converted to Unicode before it is stored in the registry.

Note that operations that access certain registry keys are redirected. For more information,  see <a href="https://msdn.microsoft.com/dace2f65-df60-419a-8be8-ab60668e6396">Registry Virtualization</a> and <a href="https://msdn.microsoft.com/08dc034c-15ce-41d9-8e74-a49b61ad40a6">32-bit and 64-bit Application Data in the Registry</a>.




## -see-also




<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a>



<a href="https://msdn.microsoft.com/ae1160be-1da7-4621-a0fc-727aa229ec06">RegFlushKey</a>



<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a>



<a href="https://msdn.microsoft.com/202d253a-10ff-40e7-8eec-a49717443b81">RegQueryValueEx</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/ffb06903-593e-47ce-adb2-baed5d379110">Registry Overview</a>
 

 

