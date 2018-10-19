---
UID: NF:winreg.RegSetValueA
title: RegSetValueA function
author: windows-sdk-content
description: Sets the data for the default or unnamed value of a specified registry key. The data must be a text string.
old-location: base\regsetvalue.htm
tech.root: sysinfo
ms.assetid: f99774d4-575b-43a3-8887-e15acb0477fd
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: RegSetValue, RegSetValue function, RegSetValueA, RegSetValueW, _win32_regsetvalue, base.regsetvalue, winreg/RegSetValue, winreg/RegSetValueA, winreg/RegSetValueW
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
req.unicode-ansi: RegSetValueW (Unicode) and RegSetValueA (ANSI)
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
 - API-MS-Win-Core-Registry-l2-1-0.dll
 - advapi32legacy.dll
 - API-MS-Win-Core-Registry-l2-2-0.dll
api_name:
 - RegSetValue
 - RegSetValueA
 - RegSetValueW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegSetValueA function


## -description


Sets the data for the default or unnamed value of a specified registry key. The data must be a text string.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should use the 
<a href="https://msdn.microsoft.com/29b0e27c-4999-4e92-bd8b-bba74920bccc">RegSetValueEx</a> function.</div><div> </div>

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
</dl>



### -param lpSubKey [in, optional]

The name of a subkey of the <i>hKey</i> parameter. The function sets the default value of the specified subkey. If <i>lpSubKey</i> does not exist, the function creates it.

Key names are not case sensitive.

If this parameter is <b>NULL</b> or points to an empty string, the function sets the default value of the key identified by <i>hKey</i>.

For more information, see 
<a href="https://msdn.microsoft.com/a6d3a884-f181-46a5-b655-226c68792e08">Registry Element Size Limits</a>.


### -param dwType [in]

The type of information to be stored. This parameter must be the REG_SZ type. To store other data types, use the 
<a href="https://msdn.microsoft.com/29b0e27c-4999-4e92-bd8b-bba74920bccc">RegSetValueEx</a> function.


### -param lpData [in]

The data to be stored. This parameter cannot be <b>NULL</b>.


### -param cbData [in]

This parameter is ignored. The function calculates this value based on the size of the data in the <i>lpData</i> parameter.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



If the key specified by the <i>lpSubKey</i> parameter does not exist, the 
<b>RegSetValue</b> function creates it.

If the ANSI version of this function is used (either by explicitly calling <b>RegSetValueA</b> or by not defining UNICODE before including the Windows.h file), the <i>lpData</i> parameter must be an ANSI character string. The string is converted to Unicode before it is stored in the registry.




## -see-also




<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a>



<a href="https://msdn.microsoft.com/ae1160be-1da7-4621-a0fc-727aa229ec06">RegFlushKey</a>



<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a>



<a href="https://msdn.microsoft.com/202d253a-10ff-40e7-8eec-a49717443b81">RegQueryValueEx</a>



<a href="https://msdn.microsoft.com/29b0e27c-4999-4e92-bd8b-bba74920bccc">RegSetValueEx</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/ffb06903-593e-47ce-adb2-baed5d379110">Registry Overview</a>
 

 

