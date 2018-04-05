---
UID: NF:winreg.RegDeleteValueA
title: RegDeleteValueA function
author: windows-driver-content
description: Removes a named value from the specified registry key.
old-location: base\regdeletevalue.htm
old-project: SysInfo
ms.assetid: 4393b4ef-cd10-40d4-bb12-2d84e7cb7d3c
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: RegDeleteValue, RegDeleteValue function, RegDeleteValueA, RegDeleteValueW, _win32_regdeletevalue, base.regdeletevalue, winreg/RegDeleteValue, winreg/RegDeleteValueA, winreg/RegDeleteValueW
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
req.unicode-ansi: RegDeleteValueW (Unicode) and RegDeleteValueA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PERF_OBJECT_TYPE, *PPERF_OBJECT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
-	API-MS-Win-Core-Localregistry-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-Registry-l1-1-0.dll
-	API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
-	API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
-	MinKernelBase.dll
-	api-ms-win-core-registry-l1-1-1.dll
api_name:
-	RegDeleteValue
-	RegDeleteValueA
-	RegDeleteValueW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RegDeleteValueA function


## -description


Removes a named value from the specified registry key. Note that value names are not case sensitive.


## -parameters




### -param hKey [in]

A handle to an open registry key. The key must have been opened with the KEY_SET_VALUE access right. For more information, see 
<a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>. 




This handle is returned by the 
<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a>, <a href="https://msdn.microsoft.com/f18e5ff9-41c3-4c26-8d01-a8ec69bcdef2">RegCreateKeyTransacted</a>, <a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a>, or 
<a href="https://msdn.microsoft.com/11663ed2-d17c-4f08-be7b-9b591271fbcd">RegOpenKeyTransacted</a> function. It can also be one of the following 
<a href="https://msdn.microsoft.com/db747656-b414-4594-ad39-6b476799060c">predefined keys</a>:


<pre xml:space="preserve"><b></b>
   <b>HKEY_CLASSES_ROOT</b>
   <b>HKEY_CURRENT_CONFIG</b>
   <b>HKEY_CURRENT_USER</b>
   <b>HKEY_LOCAL_MACHINE</b>
   <b>HKEY_USERS</b></pre>



### -param lpValueName [in, optional]

The registry value to be removed. If this parameter is <b>NULL</b> or an empty string, the value set by the 
<a href="https://msdn.microsoft.com/f99774d4-575b-43a3-8887-e15acb0477fd">RegSetValue</a> function is removed. 




For more information, see 
<a href="https://msdn.microsoft.com/a6d3a884-f181-46a5-b655-226c68792e08">Registry Element Size Limits</a>.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -see-also




<a href="https://msdn.microsoft.com/29b0e27c-4999-4e92-bd8b-bba74920bccc">RegSetValueEx</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/ffb06903-593e-47ce-adb2-baed5d379110">Registry Overview</a>
 

 

