---
UID: NF:winreg.RegDeleteKeyExA
title: RegDeleteKeyExA function
author: windows-sdk-content
description: Deletes a subkey and its values from the specified platform-specific view of the registry.
old-location: base\regdeletekeyex.htm
old-project: SysInfo
ms.assetid: 41fde6a5-647c-4293-92b8-74be54fa4136
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: KEY_WOW64_32KEY, KEY_WOW64_64KEY, RegDeleteKeyEx, RegDeleteKeyEx function, RegDeleteKeyExA, RegDeleteKeyExW, base.regdeletekeyex, winreg/RegDeleteKeyEx, winreg/RegDeleteKeyExA, winreg/RegDeleteKeyExW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP Professional x64 Edition [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegDeleteKeyExW (Unicode) and RegDeleteKeyExA (ANSI)
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
 - RegDeleteKeyEx
 - RegDeleteKeyExA
 - RegDeleteKeyExW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RegDeleteKeyExA function


## -description


Deletes a subkey and its values from the specified platform-specific view of the registry. Note that key names are not case sensitive.

To delete a subkey as a transacted operation, call the <a href="https://msdn.microsoft.com/4c67e08b-4338-4441-8300-6b6ed31d4b21">RegDeleteKeyTransacted</a> function.


## -parameters




### -param hKey [in]

A handle to an open registry key. The access rights of this key do not affect the delete operation. For more information about access rights, see 
<a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>.

This handle is returned by the 
<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a> or 
<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a> function, or it can be one of the following 
<a href="https://msdn.microsoft.com/db747656-b414-4594-ad39-6b476799060c">predefined keys</a>:<dl>
<dd><b>HKEY_CLASSES_ROOT</b></dd>
<dd><b>HKEY_CURRENT_CONFIG</b></dd>
<dd><b>HKEY_CURRENT_USER</b></dd>
<dd><b>HKEY_LOCAL_MACHINE</b></dd>
<dd><b>HKEY_USERS</b></dd>
</dl>



### -param lpSubKey [in]

The name of the key to be deleted. This key must be a subkey of the key specified by the value of the <i>hKey</i> parameter. 

The  function opens the subkey with the DELETE access right. 

Key names are not case sensitive.

The value of this parameter cannot be <b>NULL</b>.


### -param samDesired [in]

An access mask the specifies the platform-specific view of the registry.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KEY_WOW64_32KEY"></a><a id="key_wow64_32key"></a><dl>
<dt><b>KEY_WOW64_32KEY</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
Delete the key from the 32-bit registry view.

</td>
</tr>
<tr>
<td width="40%"><a id="KEY_WOW64_64KEY"></a><a id="key_wow64_64key"></a><dl>
<dt><b>KEY_WOW64_64KEY</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
Delete the key from the 64-bit registry view.

</td>
</tr>
</table>
 


### -param Reserved

This parameter is reserved and must be zero.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



A deleted key is not removed until the last handle to it is closed.

On WOW64, 32-bit applications view a registry tree that is separate from the registry tree that 64-bit applications view. This function enables an application to delete an entry in the alternate registry view.

The subkey to be deleted must not have subkeys. To delete a key and all its subkeys, you need to enumerate the subkeys and delete them individually. To delete keys recursively, use the 
<a href="https://msdn.microsoft.com/984813a9-e191-498f-8288-b8a4c567112b">RegDeleteTree</a> or <a href="_win32_shdeletekey_cpp">SHDeleteKey</a> function.

If the function succeeds, <b>RegDeleteKeyEx</b> removes the specified key from the registry. The entire key, including all of its values, is removed.




## -see-also




<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a>



<a href="https://msdn.microsoft.com/4c67e08b-4338-4441-8300-6b6ed31d4b21">RegDeleteKeyTransacted</a>



<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/b3989f79-0439-485a-96c1-4f2227d48653">Registry Redirector</a>
 

 

