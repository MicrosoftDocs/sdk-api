---
UID: NF:winreg.RegOpenKeyExW
title: RegOpenKeyExW function (winreg.h)
author: windows-sdk-content
description: Opens the specified registry key. Note that key names are not case sensitive.
old-location: base\regopenkeyex.htm
tech.root: SysInfo
ms.assetid: c8a590f2-3249-437f-a320-c7443d42b792
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: REG_OPTION_OPEN_LINK, RegOpenKeyEx, RegOpenKeyEx function, RegOpenKeyExA, RegOpenKeyExW, _win32_regopenkeyex, base.regopenkeyex, winreg/RegOpenKeyEx, winreg/RegOpenKeyExA, winreg/RegOpenKeyExW
ms.topic: function
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegOpenKeyExW (Unicode) and RegOpenKeyExA (ANSI)
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
 - RegOpenKeyEx
 - RegOpenKeyExA
 - RegOpenKeyExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegOpenKeyExW function


## -description


Opens the specified registry key. Note that key names are not case sensitive.

To perform transacted registry operations on a key, call the <a href="https://msdn.microsoft.com/11663ed2-d17c-4f08-be7b-9b591271fbcd">RegOpenKeyTransacted</a> function.


## -parameters




### -param hKey [in]

A handle to an open registry key. This handle is returned by the 
<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a> or 
<b>RegOpenKeyEx</b> function, or it can be one of the following 
<a href="https://msdn.microsoft.com/db747656-b414-4594-ad39-6b476799060c">predefined keys</a>: 




<b>HKEY_CLASSES_ROOT</b>
<b>HKEY_CURRENT_CONFIG</b>
<b>HKEY_CURRENT_USER</b>
<b>HKEY_LOCAL_MACHINE</b>
<b>HKEY_USERS</b>

### -param lpSubKey [in, optional]

The name of the registry subkey to be opened. 

Key names are not case sensitive.

The <i>lpSubKey</i> parameter can be a pointer to an empty string. If <i>lpSubKey</i> is a pointer to an empty string and <i>hKey</i> is HKEY_CLASSES_ROOT, <i>phkResult</i> receives the same <i>hKey</i> handle passed into the function. Otherwise, <i>phkResult</i> receives a new handle to the key specified by <i>hKey</i>.

The <i>lpSubKey</i> parameter can be <b>NULL</b> only if <i>hKey</i> is one of the predefined keys. If <i>lpSubKey</i> is <b>NULL</b> and <i>hKey</i> is HKEY_CLASSES_ROOT, <i>phkResult</i> receives a new handle to the key specified by <i>hKey</i>. Otherwise, <i>phkResult</i> receives the same <i>hKey</i> handle passed in to the function.

For more information, see 
<a href="https://msdn.microsoft.com/a6d3a884-f181-46a5-b655-226c68792e08">Registry Element Size Limits</a>.


### -param ulOptions [in]

Specifies the option to apply when opening the key. Set this parameter to zero or the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="REG_OPTION_OPEN_LINK"></a><a id="reg_option_open_link"></a><dl>
<dt><b>REG_OPTION_OPEN_LINK</b></dt>
</dl>
</td>
<td width="60%">
The key is a symbolic link. Registry symbolic links should only be used when absolutely necessary.

</td>
</tr>
</table>
 


### -param samDesired [in]

A mask that specifies the desired access rights to the key to be opened. The function fails if the security descriptor of the key does not permit the requested access for the calling process. For more information, see 
<a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>.


### -param phkResult [out]

A pointer to a variable that receives a handle to the opened key. If the key is not one of the predefined registry keys, call the 
<a href="https://msdn.microsoft.com/10175499-abf3-4694-9594-bb97b43f3fa5">RegCloseKey</a> function after you have finished using the handle.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



Unlike the 
<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a> function, the 
<b>RegOpenKeyEx</b> function does not create the specified key if the key does not exist in the registry.

Certain registry operations perform access checks against the security descriptor of the key, not the access mask specified when the handle to the key was obtained. For example, even if a key is opened with a <i>samDesired</i> of KEY_READ, it can be used to create registry keys if the key's security descriptor permits. In contrast, the <a href="https://msdn.microsoft.com/29b0e27c-4999-4e92-bd8b-bba74920bccc">RegSetValueEx</a> function specifically requires that the key be opened with the KEY_SET_VALUE access right.

If your service or application impersonates different users, do not use this function with <b>HKEY_CURRENT_USER</b>. Instead, call the <a href="https://msdn.microsoft.com/10a8cbfb-52dc-436a-827e-78f12eb62af0">RegOpenCurrentUser</a> function.

Note that operations that access certain registry keys are redirected. For more information,  see <a href="https://msdn.microsoft.com/dace2f65-df60-419a-8be8-ab60668e6396">Registry Virtualization</a> and <a href="https://msdn.microsoft.com/08dc034c-15ce-41d9-8e74-a49b61ad40a6">32-bit and 64-bit Application Data in the Registry</a>.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/1cf6db95-85a4-4416-b17e-e14f45804503">Deleting a Key with Subkeys</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/10175499-abf3-4694-9594-bb97b43f3fa5">RegCloseKey</a>



<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a>



<a href="https://msdn.microsoft.com/a2310ca0-1b9f-48d1-a3b5-ea3a528bfaba">RegDeleteKey</a>



<a href="https://msdn.microsoft.com/11663ed2-d17c-4f08-be7b-9b591271fbcd">RegOpenKeyTransacted</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/ffb06903-593e-47ce-adb2-baed5d379110">Registry Overview</a>
 

 

