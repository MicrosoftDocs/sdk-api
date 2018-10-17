---
UID: NF:winreg.RegDeleteKeyValueA
title: RegDeleteKeyValueA function
author: windows-sdk-content
description: Removes the specified value from the specified registry key and subkey.
old-location: base\regdeletekeyvalue.htm
tech.root: sysinfo
ms.assetid: a4a082c2-8cf3-41eb-87c0-a6c453821f8b
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: RegDeleteKeyValue, RegDeleteKeyValue function, RegDeleteKeyValueA, RegDeleteKeyValueW, base.regdeletekeyvalue, winreg/RegDeleteKeyValue, winreg/RegDeleteKeyValueA, winreg/RegDeleteKeyValueW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegDeleteKeyValueW (Unicode) and RegDeleteKeyValueA (ANSI)
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
 - API-MS-Win-Core-Registry-l1-1-1.dll
 - KernelBase.dll
 - MinKernelBase.dll
api_name:
 - RegDeleteKeyValue
 - RegDeleteKeyValueA
 - RegDeleteKeyValueW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegDeleteKeyValueA function


## -description


Removes the specified  value from the specified registry key and subkey.


## -parameters




### -param hKey [in]

A handle to an open registry key. The key must have been opened with the KEY_SET_VALUE access right. For more information, see 
<a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>. 




This handle is returned by the 
<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a> or 
<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a> function, or it can be one of the following 
<a href="https://msdn.microsoft.com/db747656-b414-4594-ad39-6b476799060c">predefined keys</a>:


<pre xml:space="preserve"><b></b>
   <b>HKEY_CLASSES_ROOT</b>
   <b>HKEY_CURRENT_CONFIG</b>
   <b>HKEY_CURRENT_USER</b>
   <b>HKEY_LOCAL_MACHINE</b>
   <b>HKEY_USERS</b></pre>



### -param lpSubKey [in, optional]

The name of the registry key. This key must be a subkey of the key identified by the <i>hKey</i> parameter.


### -param lpValueName [in, optional]

The registry value to be removed from the key.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/e27d2dd6-b139-4ac1-8dd8-527022333364">RegSetKeyValue</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>
 

 

