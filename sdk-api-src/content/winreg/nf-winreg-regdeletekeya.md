---
UID: NF:winreg.RegDeleteKeyA
title: RegDeleteKeyA function
author: windows-sdk-content
description: Deletes a subkey and its values.
old-location: base\regdeletekey.htm
tech.root: SysInfo
ms.assetid: a2310ca0-1b9f-48d1-a3b5-ea3a528bfaba
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RegDeleteKey, RegDeleteKey function, RegDeleteKeyA, RegDeleteKeyW, _win32_regdeletekey, base.regdeletekey, winreg/RegDeleteKey, winreg/RegDeleteKeyA, winreg/RegDeleteKeyW
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
req.unicode-ansi: RegDeleteKeyW (Unicode) and RegDeleteKeyA (ANSI)
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
 - API-MS-Win-Deprecated-apis-advapi-l1-1-0.dll
 - API-MS-Win-Core-Registry-l2-2-0.dll
api_name:
 - RegDeleteKey
 - RegDeleteKeyA
 - RegDeleteKeyW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegDeleteKeyA function


## -description


Deletes a subkey and its values. Note that key names are not case sensitive.

<b>64-bit Windows:  </b>On WOW64, 32-bit applications view a registry tree that is separate from the registry tree that 64-bit applications view. To enable an application to delete an entry in the alternate registry view, use the <a href="https://msdn.microsoft.com/41fde6a5-647c-4293-92b8-74be54fa4136">RegDeleteKeyEx</a> function.


## -parameters




### -param hKey [in]

A handle to an open registry key. The access rights of this key do not affect the delete operation. For more information about access rights, see 
<a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>.

This handle is returned by the 
<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a> or 
<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a> function, or it can be one of the following 
<a href="https://msdn.microsoft.com/db747656-b414-4594-ad39-6b476799060c">Predefined Keys</a>:<dl>
<dd><b>HKEY_CLASSES_ROOT</b></dd>
<dd><b>HKEY_CURRENT_CONFIG</b></dd>
<dd><b>HKEY_CURRENT_USER</b></dd>
<dd><b>HKEY_LOCAL_MACHINE</b></dd>
<dd><b>HKEY_USERS</b></dd>
</dl>



### -param lpSubKey [in]

The name of the key to be deleted. It must be a subkey of the key that <i>hKey</i> identifies, but it cannot have subkeys. This parameter cannot be <b>NULL</b>.

The function opens the subkey with the DELETE access right. 

Key names are not case sensitive.

For more information, see 
<a href="https://msdn.microsoft.com/a6d3a884-f181-46a5-b655-226c68792e08">Registry Element Size Limits</a>.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. To get a generic description of the error, you can use the 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag.




## -remarks



A deleted key is not removed until the last handle to it is closed.

The subkey to be deleted must not have subkeys. To delete a key and all its subkeys, you need to enumerate the subkeys and delete them individually. To delete keys recursively, use the 
<a href="https://msdn.microsoft.com/984813a9-e191-498f-8288-b8a4c567112b">RegDeleteTree</a> or <a href="_win32_shdeletekey_cpp">SHDeleteKey</a> function.


#### Examples

For an example that uses this function, see <a href="https://msdn.microsoft.com/1cf6db95-85a4-4416-b17e-e14f45804503">Deleting a Key with Subkeys</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/10175499-abf3-4694-9594-bb97b43f3fa5">RegCloseKey</a>



<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a>



<a href="https://msdn.microsoft.com/984813a9-e191-498f-8288-b8a4c567112b">RegDeleteTree</a>



<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/ffb06903-593e-47ce-adb2-baed5d379110">Registry Overview</a>



<a href="https://msdn.microsoft.com/6a560bc3-f65e-4b7d-9fbc-b4f2971ce2a9">SHDeleteEmptyKey</a>



<a href="_win32_shdeletekey_cpp">SHDeleteKey</a>
 

 

