---
UID: NF:winreg.RegOpenKeyExW
title: RegOpenKeyExW function (winreg.h)
description: Opens the specified registry key. Note that key names are not case sensitive.
old-location: base\regopenkeyex.htm
tech.root: SysInfo
ms.assetid: c8a590f2-3249-437f-a320-c7443d42b792
ms.date: 12/05/2018
ms.keywords: REG_OPTION_OPEN_LINK, RegOpenKeyEx, RegOpenKeyEx function, RegOpenKeyExA, RegOpenKeyExW, _win32_regopenkeyex, base.regopenkeyex, winreg/RegOpenKeyEx, winreg/RegOpenKeyExA, winreg/RegOpenKeyExW
ms.topic: function
f1_keywords:
- winreg/RegOpenKeyEx
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RegOpenKeyExW function


## -description


Opens the specified registry key. Note that key names are not case sensitive.

To perform transacted registry operations on a key, call the <a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regopenkeytransacteda">RegOpenKeyTransacted</a> function.


## -parameters




### -param hKey [in]

A handle to an open registry key. This handle is returned by the 
<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a> or 
<b>RegOpenKeyEx</b> function, or it can be one of the following 
<a href="https://docs.microsoft.com/windows/desktop/SysInfo/predefined-keys">predefined keys</a>: 




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
<a href="https://docs.microsoft.com/windows/desktop/SysInfo/registry-element-size-limits">Registry Element Size Limits</a>.


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
<a href="https://docs.microsoft.com/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.


### -param phkResult [out]

A pointer to a variable that receives a handle to the opened key. If the key is not one of the predefined registry keys, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regclosekey">RegCloseKey</a> function after you have finished using the handle.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



Unlike the 
<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a> function, the 
<b>RegOpenKeyEx</b> function does not create the specified key if the key does not exist in the registry.

Certain registry operations perform access checks against the security descriptor of the key, not the access mask specified when the handle to the key was obtained. For example, even if a key is opened with a <i>samDesired</i> of KEY_READ, it can be used to create registry keys if the key's security descriptor permits. In contrast, the <a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regsetvalueexa">RegSetValueEx</a> function specifically requires that the key be opened with the KEY_SET_VALUE access right.

If your service or application impersonates different users, do not use this function with <b>HKEY_CURRENT_USER</b>. Instead, call the <a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regopencurrentuser">RegOpenCurrentUser</a> function.

Note that operations that access certain registry keys are redirected. For more information,  see <a href="https://docs.microsoft.com/windows/desktop/SysInfo/registry-virtualization">Registry Virtualization</a> and <a href="https://docs.microsoft.com/windows/desktop/SysInfo/32-bit-and-64-bit-application-data-in-the-registry">32-bit and 64-bit Application Data in the Registry</a>.


#### Examples

For an example, see 
<a href="https://docs.microsoft.com/windows/desktop/SysInfo/deleting-a-key-with-subkeys">Deleting a Key with Subkeys</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regclosekey">RegCloseKey</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regdeletekeya">RegDeleteKey</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regopenkeytransacteda">RegOpenKeyTransacted</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/registry">Registry Overview</a>
 

 

