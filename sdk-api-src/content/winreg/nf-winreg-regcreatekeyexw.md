---
UID: NF:winreg.RegCreateKeyExW
title: RegCreateKeyExW function
author: windows-sdk-content
description: Creates the specified registry key. If the key already exists, the function opens it. Note that key names are not case sensitive.
old-location: base\regcreatekeyex.htm
old-project: sysinfo
ms.assetid: e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: REG_CREATED_NEW_KEY, REG_OPENED_EXISTING_KEY, REG_OPTION_BACKUP_RESTORE, REG_OPTION_CREATE_LINK, REG_OPTION_NON_VOLATILE, REG_OPTION_VOLATILE, RegCreateKeyEx, RegCreateKeyEx function, RegCreateKeyExA, RegCreateKeyExW, _win32_regcreatekeyex, base.regcreatekeyex, winreg/RegCreateKeyEx, winreg/RegCreateKeyExA, winreg/RegCreateKeyExW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winreg.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegCreateKeyExW (Unicode) and RegCreateKeyExA (ANSI)
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
 - RegCreateKeyEx
 - RegCreateKeyExA
 - RegCreateKeyExW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RegCreateKeyExW function


## -description


Creates the specified registry key. If the key already exists, the function opens it. Note that key names are not case sensitive.

To perform transacted registry operations on a key, call the <a href="https://msdn.microsoft.com/f18e5ff9-41c3-4c26-8d01-a8ec69bcdef2">RegCreateKeyTransacted</a> function.

 Applications that back up or restore system state including system files and registry hives should use the <a href="http://go.microsoft.com/fwlink/p/?linkid=177790">Volume Shadow Copy Service</a> instead of the registry functions.


## -parameters




### -param hKey [in]

A handle to an open registry key. The calling process  must have KEY_CREATE_SUB_KEY access to the key. For more information, see 
<a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>.

Access for key creation is checked against the security descriptor of the registry key, not the access mask specified when the handle was obtained. Therefore, even if <i>hKey</i> was opened with a <i>samDesired</i> of KEY_READ, it   can be used in operations that modify the registry if allowed by its security descriptor.

This handle is returned by the 
<b>RegCreateKeyEx</b> or 
<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a> function, or it can be one of the following 
<a href="https://msdn.microsoft.com/db747656-b414-4594-ad39-6b476799060c">predefined keys</a>: 


<dl>
<dd><b>HKEY_CLASSES_ROOT</b></dd>
<dd><b>HKEY_CURRENT_CONFIG</b></dd>
<dd><b>HKEY_CURRENT_USER</b></dd>
<dd><b>HKEY_LOCAL_MACHINE</b></dd>
<dd><b>HKEY_USERS</b></dd>
</dl>



### -param lpSubKey [in]

The name of a subkey that this function opens or creates. The subkey specified must be a subkey of the key identified by the <i>hKey</i> parameter; it can be up to 32 levels deep in the registry tree. For more information on key names, see <a href="https://msdn.microsoft.com/4ed60563-73d8-4134-8cb2-8388734fb18d">Structure of the Registry</a>.

If <i>lpSubKey</i> is a pointer to an empty string, <i>phkResult</i> receives a new handle to the key specified by <i>hKey</i>.

This parameter cannot be <b>NULL</b>.


### -param Reserved

This parameter is reserved and must be zero.


### -param lpClass [in, optional]

The user-defined class type of this key. This parameter may be ignored. This parameter can be <b>NULL</b>.


### -param dwOptions [in]

This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="REG_OPTION_BACKUP_RESTORE"></a><a id="reg_option_backup_restore"></a><dl>
<dt><b>REG_OPTION_BACKUP_RESTORE</b></dt>
<dt>0x00000004L</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the function ignores the <i>samDesired</i> parameter and attempts to open the key with the access required to backup or restore the key. If the calling thread has the SE_BACKUP_NAME privilege enabled, the key is opened with the ACCESS_SYSTEM_SECURITY and KEY_READ access rights. If the calling thread has the SE_RESTORE_NAME privilege enabled, beginning with Windows Vista, the key is opened with the ACCESS_SYSTEM_SECURITY, DELETE and KEY_WRITE access rights. If both privileges are enabled, the key has the combined access rights for both privileges. For more information, see 
<a href="https://msdn.microsoft.com/b25db548-d5ab-4276-9b50-36d030909384">Running with Special Privileges</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="REG_OPTION_CREATE_LINK"></a><a id="reg_option_create_link"></a><dl>
<dt><b>REG_OPTION_CREATE_LINK</b></dt>
<dt>0x00000002L</dt>
</dl>
</td>
<td width="60%">
<div class="alert"><b>Note</b>  Registry symbolic links should only be used for  for application compatibility when <u>absolutely</u> necessary. </div>
<div> </div>
This key is a symbolic link. The target path is assigned to the L"SymbolicLinkValue" value of the key. The target path must be an absolute registry path. 

</td>
</tr>
<tr>
<td width="40%"><a id="REG_OPTION_NON_VOLATILE"></a><a id="reg_option_non_volatile"></a><dl>
<dt><b>REG_OPTION_NON_VOLATILE</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
This key is not volatile; this is the default. The information is stored in a file and is preserved when the system is restarted. The 
<a href="https://msdn.microsoft.com/da80f40d-0099-4748-94ca-5d3b001e633e">RegSaveKey</a> function saves keys that are not volatile.

</td>
</tr>
<tr>
<td width="40%"><a id="REG_OPTION_VOLATILE"></a><a id="reg_option_volatile"></a><dl>
<dt><b>REG_OPTION_VOLATILE</b></dt>
<dt>0x00000001L</dt>
</dl>
</td>
<td width="60%">
All keys created by the function are volatile. The information is stored in memory and is not preserved when the corresponding registry hive is unloaded. For <b>HKEY_LOCAL_MACHINE</b>, this occurs only when the system initiates a full shutdown. For registry keys loaded by the 
<a href="https://msdn.microsoft.com/536395aa-03ba-430d-a66d-fcabdc9dfe22">RegLoadKey</a> function, this occurs when the corresponding 
<a href="https://msdn.microsoft.com/73b4b6a9-4acb-4247-bd7f-82024ba3e14a">RegUnLoadKey</a> is performed. The 
<a href="https://msdn.microsoft.com/da80f40d-0099-4748-94ca-5d3b001e633e">RegSaveKey</a> function does not save volatile keys. This flag is ignored for keys that already exist. 



							

<div class="alert"><b>Note</b>  On a user selected shutdown,
a fast startup shutdown is the default behavior for the system.</div>
<div> </div>
</td>
</tr>
</table>
 


### -param samDesired [in]

A mask that specifies the access rights for the key to be created. For more information, see 
<a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>.


### -param lpSecurityAttributes [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> structure that determines whether the returned handle can be inherited by child processes. If <i>lpSecurityAttributes</i> is <b>NULL</b>, the handle cannot be inherited. 




The <b>lpSecurityDescriptor</b> member of the structure specifies a security descriptor for the new key. If <i>lpSecurityAttributes</i> is <b>NULL</b>, the key gets a default security descriptor. The ACLs in a default security descriptor for a key are inherited from its direct parent key.


### -param phkResult [out]

A pointer to a variable that receives a handle to the opened or created key. If the key is not one of the predefined registry keys, call the 
<a href="https://msdn.microsoft.com/10175499-abf3-4694-9594-bb97b43f3fa5">RegCloseKey</a> function after you have finished using the handle.


### -param lpdwDisposition [out, optional]

A pointer to a variable that receives one of the following disposition values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="REG_CREATED_NEW_KEY"></a><a id="reg_created_new_key"></a><dl>
<dt><b>REG_CREATED_NEW_KEY</b></dt>
<dt>0x00000001L</dt>
</dl>
</td>
<td width="60%">
The key did not exist and was created.

</td>
</tr>
<tr>
<td width="40%"><a id="REG_OPENED_EXISTING_KEY"></a><a id="reg_opened_existing_key"></a><dl>
<dt><b>REG_OPENED_EXISTING_KEY</b></dt>
<dt>0x00000002L</dt>
</dl>
</td>
<td width="60%">
The key existed and was simply opened without being changed.

</td>
</tr>
</table>
 

If <i>lpdwDisposition</i> is <b>NULL</b>, no disposition information is returned.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



The key that the 
<b>RegCreateKeyEx</b> function creates has no values. An application can use the 
<a href="https://msdn.microsoft.com/29b0e27c-4999-4e92-bd8b-bba74920bccc">RegSetValueEx</a> function to set key values.

The <b>RegCreateKeyEx</b> function creates all missing keys in the specified path. An application can take advantage of this behavior to create several keys at once. For example, an application can create a subkey four levels deep at the same time as the three preceding subkeys by specifying a string of the following form for the <i>lpSubKey</i> parameter:

<i>subkey1\subkey2\subkey3\subkey4
			</i>

Note that this behavior will result in creation of unwanted keys if an existing key in the path is spelled incorrectly. 

An application cannot create a key that is a direct child of <b>HKEY_USERS</b> or <b>HKEY_LOCAL_MACHINE</b>. An application can create subkeys in lower levels of the <b>HKEY_USERS</b> or <b>HKEY_LOCAL_MACHINE</b> trees.

If your service or application impersonates different users, do not use this function with <b>HKEY_CURRENT_USER</b>. Instead, call the <a href="https://msdn.microsoft.com/10a8cbfb-52dc-436a-827e-78f12eb62af0">RegOpenCurrentUser</a> function.

Note that operations that access certain registry keys are redirected. For more information,  see <a href="https://msdn.microsoft.com/dace2f65-df60-419a-8be8-ab60668e6396">Registry Virtualization</a> and <a href="https://msdn.microsoft.com/08dc034c-15ce-41d9-8e74-a49b61ad40a6">32-bit and 64-bit Application Data in the Registry</a>.




## -see-also




<a href="https://msdn.microsoft.com/10175499-abf3-4694-9594-bb97b43f3fa5">RegCloseKey</a>



<a href="https://msdn.microsoft.com/a2310ca0-1b9f-48d1-a3b5-ea3a528bfaba">RegDeleteKey</a>



<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a>



<a href="https://msdn.microsoft.com/da80f40d-0099-4748-94ca-5d3b001e633e">RegSaveKey</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/ffb06903-593e-47ce-adb2-baed5d379110">Registry Overview</a>



<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>
 

 

