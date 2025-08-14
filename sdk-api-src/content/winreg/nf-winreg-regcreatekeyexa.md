---
UID: NF:winreg.RegCreateKeyExA
title: RegCreateKeyExA function (winreg.h)
description: Creates the specified registry key. If the key already exists, the function opens it. Note that key names are not case sensitive. (ANSI)
helpviewer_keywords: ["REG_CREATED_NEW_KEY", "REG_OPENED_EXISTING_KEY", "REG_OPTION_BACKUP_RESTORE", "REG_OPTION_CREATE_LINK", "REG_OPTION_NON_VOLATILE", "REG_OPTION_VOLATILE", "RegCreateKeyExA", "winreg/RegCreateKeyExA"]
old-location: base\regcreatekeyex.htm
tech.root: winprog
ms.assetid: e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4
ms.date: 12/05/2018
ms.keywords: REG_CREATED_NEW_KEY, REG_OPENED_EXISTING_KEY, REG_OPTION_BACKUP_RESTORE, REG_OPTION_CREATE_LINK, REG_OPTION_NON_VOLATILE, REG_OPTION_VOLATILE, RegCreateKeyEx, RegCreateKeyEx function, RegCreateKeyExA, RegCreateKeyExW, _win32_regcreatekeyex, base.regcreatekeyex, winreg/RegCreateKeyEx, winreg/RegCreateKeyExA, winreg/RegCreateKeyExW
req.header: winreg.h
req.include-header: Windows.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegCreateKeyExA
 - winreg/RegCreateKeyExA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-registry-l1-1-2.dll
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
---

# RegCreateKeyExA function


## -description

Creates the specified registry key. If the key already exists, the function opens it. Note that key names are not case sensitive.

To perform transacted registry operations on a key, call the <a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeytransacteda">RegCreateKeyTransacted</a> function.

 Applications that back up or restore system state including system files and registry hives should use the <a href="/windows/win32/vss/volume-shadow-copy-service-overview">Volume Shadow Copy Service</a> instead of the registry functions.

## -parameters

### -param hKey [in]

A handle to an open registry key. The calling process  must have KEY_CREATE_SUB_KEY access to the key. For more information, see 
<a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.

Access for key creation is checked against the security descriptor of the registry key, not the access mask specified when the handle was obtained. Therefore, even if <i>hKey</i> was opened with a <i>samDesired</i> of KEY_READ, it   can be used in operations that modify the registry if allowed by its security descriptor.

This handle is returned by the 
<b>RegCreateKeyEx</b> or 
<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a> function, or it can be one of the following 
<a href="/windows/desktop/SysInfo/predefined-keys">predefined keys</a>: 


<dl>
<dd><b>HKEY_CLASSES_ROOT</b></dd>
<dd><b>HKEY_CURRENT_CONFIG</b></dd>
<dd><b>HKEY_CURRENT_USER</b></dd>
<dd><b>HKEY_LOCAL_MACHINE</b></dd>
<dd><b>HKEY_USERS</b></dd>
</dl>

### -param lpSubKey [in]

The name of a subkey that this function opens or creates. The subkey specified must be a subkey of the key identified by the <i>hKey</i> parameter; it can be up to 32 levels deep in the registry tree. For more information on key names, see <a href="/windows/desktop/SysInfo/structure-of-the-registry">Structure of the Registry</a>.

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
<a href="/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="REG_OPTION_CREATE_LINK"></a><a id="reg_option_create_link"></a><dl>
<dt><b>REG_OPTION_CREATE_LINK</b></dt>
<dt>0x00000002L</dt>
</dl>
</td>
<td width="60%">
<div class="alert"><b>Note</b>  Registry symbolic links should only be used for application compatibility when <u>absolutely</u> necessary. </div>
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
<a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya">RegSaveKey</a> function saves keys that are not volatile.

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
<a href="/windows/desktop/api/winreg/nf-winreg-regloadkeya">RegLoadKey</a> function, this occurs when the corresponding 
<a href="/windows/desktop/api/winreg/nf-winreg-regunloadkeya">RegUnLoadKey</a> is performed. The 
<a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya">RegSaveKey</a> function does not save volatile keys. This flag is ignored for keys that already exist. 



							

<div class="alert"><b>Note</b>  On a user selected shutdown,
a fast startup shutdown is the default behavior for the system.</div>
<div> </div>
</td>
</tr>
</table>

### -param samDesired [in]

A mask that specifies the access rights for the key to be created. For more information, see 
<a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.

### -param lpSecurityAttributes [in, optional]

A pointer to a 
<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure that determines whether the returned handle can be inherited by child processes. If <i>lpSecurityAttributes</i> is <b>NULL</b>, the handle cannot be inherited. 




The <b>lpSecurityDescriptor</b> member of the structure specifies a security descriptor for the new key. If <i>lpSecurityAttributes</i> is <b>NULL</b>, the key gets a default security descriptor. The ACLs in a default security descriptor for a key are inherited from its direct parent key.

### -param phkResult [out]

A pointer to a variable that receives a handle to the opened or created key. If the key is not one of the predefined registry keys, call the 
<a href="/windows/desktop/api/winreg/nf-winreg-regclosekey">RegCloseKey</a> function after you have finished using the handle.

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
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.

## -remarks

The key that the 
<b>RegCreateKeyEx</b> function creates has no values. An application can use the 
<a href="/windows/desktop/api/winreg/nf-winreg-regsetvalueexa">RegSetValueEx</a> function to set key values.

The <b>RegCreateKeyEx</b> function creates all missing keys in the specified path. An application can take advantage of this behavior to create several keys at once. For example, an application can create a subkey four levels deep at the same time as the three preceding subkeys by specifying a string of the following form for the <i>lpSubKey</i> parameter:

<i>subkey1\subkey2\subkey3\subkey4
			</i>

Note that this behavior will result in creation of unwanted keys if an existing key in the path is spelled incorrectly. 

An application cannot create a key that is a direct child of <b>HKEY_USERS</b> or <b>HKEY_LOCAL_MACHINE</b>. An application can create subkeys in lower levels of the <b>HKEY_USERS</b> or <b>HKEY_LOCAL_MACHINE</b> trees.

If your service or application impersonates different users, do not use this function with <b>HKEY_CURRENT_USER</b>. Instead, call the <a href="/windows/desktop/api/winreg/nf-winreg-regopencurrentuser">RegOpenCurrentUser</a> function.

Note that operations that access certain registry keys are redirected. For more information,  see <a href="/windows/desktop/SysInfo/registry-virtualization">Registry Virtualization</a> and <a href="/windows/desktop/SysInfo/32-bit-and-64-bit-application-data-in-the-registry">32-bit and 64-bit Application Data in the Registry</a>.





> [!NOTE]
> The winreg.h header defines RegCreateKeyEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regclosekey">RegCloseKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regdeletekeya">RegDeleteKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya">RegSaveKey</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="/windows/desktop/SysInfo/registry">Registry Overview</a>



<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a>
