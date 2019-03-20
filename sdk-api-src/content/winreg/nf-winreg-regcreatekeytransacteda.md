---
UID: NF:winreg.RegCreateKeyTransactedA
title: RegCreateKeyTransactedA function (winreg.h)
author: windows-sdk-content
description: Creates the specified registry key and associates it with a transaction.
old-location: base\regcreatekeytransacted.htm
tech.root: SysInfo
ms.assetid: f18e5ff9-41c3-4c26-8d01-a8ec69bcdef2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: REG_CREATED_NEW_KEY, REG_OPENED_EXISTING_KEY, REG_OPTION_BACKUP_RESTORE, REG_OPTION_NON_VOLATILE, REG_OPTION_VOLATILE, RegCreateKeyTransacted, RegCreateKeyTransacted function, RegCreateKeyTransactedA, RegCreateKeyTransactedW, base.regcreatekeytransacted, winreg/RegCreateKeyTransacted, winreg/RegCreateKeyTransactedA, winreg/RegCreateKeyTransactedW
ms.topic: function
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegCreateKeyTransactedW (Unicode) and RegCreateKeyTransactedA (ANSI)
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
 - RegCreateKeyTransacted
 - RegCreateKeyTransactedA
 - RegCreateKeyTransactedW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegCreateKeyTransactedA function


## -description


Creates the specified registry key and associates it with a  transaction. If the key already exists, the function opens it. Note that key names are not case sensitive.

 Applications that back up or restore system state including system files and registry hives should use the <a href="http://go.microsoft.com/fwlink/p/?linkid=177790">Volume Shadow Copy Service</a> instead of the registry functions.


## -parameters




### -param hKey [in]

A handle to an open registry key. The calling process  must have KEY_CREATE_SUB_KEY access to the key. For more information, see 
<a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>.

Access for key creation is checked against the security descriptor of the registry key, not the access mask specified when the handle was obtained. Therefore, even if <i>hKey</i> was opened with a <i>samDesired</i> of KEY_READ, it   can be used in operations that create keys if allowed by its security descriptor.

This handle is returned by the 
<b>RegCreateKeyTransacted</b> or 
<a href="https://msdn.microsoft.com/11663ed2-d17c-4f08-be7b-9b591271fbcd">RegOpenKeyTransacted</a> function, or it can be one of the following 
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

The user-defined class of this key. This parameter may be ignored. This parameter can be <b>NULL</b>.


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
If this flag is set, the function ignores the <i>samDesired</i> parameter and attempts to open the key with the access required to backup or restore the key. If the calling thread has the SE_BACKUP_NAME privilege enabled, the key is opened with the ACCESS_SYSTEM_SECURITY and KEY_READ access rights. If the calling thread has the SE_RESTORE_NAME privilege enabled, the key is opened with the ACCESS_SYSTEM_SECURITY and KEY_WRITE access rights. If both privileges are enabled, the key has the combined access rights for both privileges. For more information, see 
<a href="https://msdn.microsoft.com/b25db548-d5ab-4276-9b50-36d030909384">Running with Special Privileges</a>.

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
All keys created by the function are volatile. The information is stored in memory and is not preserved when the corresponding registry hive is unloaded. For <b>HKEY_LOCAL_MACHINE</b>, this occurs when the system is shut down. For registry keys loaded by the 
<a href="https://msdn.microsoft.com/536395aa-03ba-430d-a66d-fcabdc9dfe22">RegLoadKey</a> function, this occurs when the corresponding 
<a href="https://msdn.microsoft.com/73b4b6a9-4acb-4247-bd7f-82024ba3e14a">RegUnLoadKey</a> is performed. The 
<a href="https://msdn.microsoft.com/da80f40d-0099-4748-94ca-5d3b001e633e">RegSaveKey</a> function does not save volatile keys. This flag is ignored for keys that already exist.

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


### -param hTransaction [in]

A handle to an active transaction. This handle is returned by the <a href="https://msdn.microsoft.com/578bda35-bd35-4f6d-8366-a4bfb4dbfe42">CreateTransaction</a> function.


### -param pExtendedParemeter

This parameter is reserved and must be <b>NULL</b>.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



When a key is created using this function, subsequent operations on the key are transacted. If a non-transacted operation is performed on the key before the transaction is committed, the transaction is rolled back. After a transaction is committed or rolled back, you must re-open the key using <b>RegCreateKeyTransacted</b> or <a href="https://msdn.microsoft.com/11663ed2-d17c-4f08-be7b-9b591271fbcd">RegOpenKeyTransacted</a> with an active transaction handle to make additional operations transacted. For more information about transactions, see <a href="https://msdn.microsoft.com/en-us/library/Bb986748(v=VS.85).aspx">Kernel Transaction Manager</a>.

Note that subsequent operations on subkeys of this key are not automatically transacted. Therefore,  <a href="https://msdn.microsoft.com/41fde6a5-647c-4293-92b8-74be54fa4136">RegDeleteKeyEx</a> does not perform a transacted delete operation. Instead, use the <a href="https://msdn.microsoft.com/4c67e08b-4338-4441-8300-6b6ed31d4b21">RegDeleteKeyTransacted</a> function to perform a transacted delete operation.

The key that the 
<b>RegCreateKeyTransacted</b> function creates has no values. An application can use the 
<a href="https://msdn.microsoft.com/29b0e27c-4999-4e92-bd8b-bba74920bccc">RegSetValueEx</a> function to set key values.

The <b>RegCreateKeyTransacted</b> function creates all missing keys in the specified path. An application can take advantage of this behavior to create several keys at once. For example, an application can create a subkey four levels deep at the same time as the three preceding subkeys by specifying a string of the following form for the <i>lpSubKey</i> parameter:

<i>subkey1\subkey2\subkey3\subkey4
			</i>

Note that this behavior will result in creation of unwanted keys if an existing key in the path is spelled incorrectly. 

An application cannot create a key that is a direct child of <b>HKEY_USERS</b> or <b>HKEY_LOCAL_MACHINE</b>. An application can create subkeys in lower levels of the <b>HKEY_USERS</b> or <b>HKEY_LOCAL_MACHINE</b> trees.




## -see-also




<a href="https://msdn.microsoft.com/10175499-abf3-4694-9594-bb97b43f3fa5">RegCloseKey</a>



<a href="https://msdn.microsoft.com/4c67e08b-4338-4441-8300-6b6ed31d4b21">RegDeleteKeyTransacted</a>



<a href="https://msdn.microsoft.com/11663ed2-d17c-4f08-be7b-9b591271fbcd">RegOpenKeyTransacted</a>



<a href="https://msdn.microsoft.com/da80f40d-0099-4748-94ca-5d3b001e633e">RegSaveKey</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/ffb06903-593e-47ce-adb2-baed5d379110">Registry Overview</a>



<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>
 

 

