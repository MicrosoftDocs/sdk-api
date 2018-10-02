---
UID: NF:winreg.RegSetKeyValueW
title: RegSetKeyValueW function
author: windows-sdk-content
description: Sets the data for the specified value in the specified registry key and subkey.
old-location: base\regsetkeyvalue.htm
tech.root: SysInfo
ms.assetid: e27d2dd6-b139-4ac1-8dd8-527022333364
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: RegSetKeyValue, RegSetKeyValue function, RegSetKeyValueA, RegSetKeyValueW, base.regsetkeyvalue, winreg/RegSetKeyValue, winreg/RegSetKeyValueA, winreg/RegSetKeyValueW
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
req.unicode-ansi: RegSetKeyValueW (Unicode) and RegSetKeyValueA (ANSI)
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
 - RegSetKeyValue
 - RegSetKeyValueA
 - RegSetKeyValueW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegSetKeyValueW function


## -description


Sets the data for the specified value in the specified registry key and subkey.


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



### -param lpSubKey [in, optional]

The name of a key and a subkey to the key identified by <i>hKey</i>. If this parameter is <b>NULL</b>, then this value is created in the key using the <i>hKey</i> value and the key gets a default security descriptor.


### -param lpValueName [in, optional]

The name of the registry value whose data is to be updated.


### -param dwType [in]

The type of data pointed to by the <i>lpData</i> parameter. For a list of the possible types, see 
<a href="https://msdn.microsoft.com/5fd828d6-4d62-4823-a2f1-15782b5cd28c">Registry Value Types</a>.


### -param lpData [in, optional]

The data to be stored with the specified value name. 

For string-based types, such as REG_SZ, the string must be null-terminated. With the REG_MULTI_SZ data type, the string must be terminated with two null characters.


### -param cbData [in]

The size of the information pointed to by the <i>lpData</i> parameter, in bytes. If the data is of type REG_SZ, REG_EXPAND_SZ, or REG_MULTI_SZ, <i>cbData</i> must include the size of the terminating null character or characters.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/a4a082c2-8cf3-41eb-87c0-a6c453821f8b">RegDeleteKeyValue</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>
 

 

