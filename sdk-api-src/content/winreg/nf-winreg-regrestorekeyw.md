---
UID: NF:winreg.RegRestoreKeyW
title: RegRestoreKeyW function
author: windows-sdk-content
description: Reads the registry information in a specified file and copies it over the specified key. This registry information may be in the form of a key and multiple levels of subkeys.
old-location: base\regrestorekey.htm
tech.root: sysinfo
ms.assetid: 6267383d-427a-4ae8-b9cc-9c1861d3b7bb
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: REG_FORCE_RESTORE, REG_WHOLE_HIVE_VOLATILE, RegRestoreKey, RegRestoreKey function, RegRestoreKeyA, RegRestoreKeyW, _win32_regrestorekey, base.regrestorekey, winreg/RegRestoreKey, winreg/RegRestoreKeyA, winreg/RegRestoreKeyW
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
req.unicode-ansi: RegRestoreKeyW (Unicode) and RegRestoreKeyA (ANSI)
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
 - RegRestoreKey
 - RegRestoreKeyA
 - RegRestoreKeyW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegRestoreKeyW function


## -description


Reads the registry information in a specified file and copies it over the specified key. This registry information may be in the form of a key and multiple levels of subkeys.

 Applications that back up or restore system state including system files and registry hives should use the <a href="http://go.microsoft.com/fwlink/p/?linkid=177790">Volume Shadow Copy Service</a> instead of the registry functions.


## -parameters




### -param hKey [in]

A handle to an open registry key. This handle is returned by the 
<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a> or <a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a> function. It can also be one of the following 
<a href="https://msdn.microsoft.com/db747656-b414-4594-ad39-6b476799060c">predefined keys</a>: 




<b>HKEY_CLASSES_ROOT</b>
<b>HKEY_CURRENT_CONFIG</b>
<b>HKEY_CURRENT_USER</b>
<b>HKEY_LOCAL_MACHINE</b>
<b>HKEY_USERS</b>
Any information contained in this key and its descendent keys is overwritten by the information in the file pointed to by the <i>lpFile</i> parameter.


### -param lpFile [in]

The name of the file with the registry information. This file is typically created by using the 
<a href="https://msdn.microsoft.com/da80f40d-0099-4748-94ca-5d3b001e633e">RegSaveKey</a> function.


### -param dwFlags [in]

The flags that indicate how the key or keys are to be restored. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="REG_FORCE_RESTORE"></a><a id="reg_force_restore"></a><dl>
<dt><b>REG_FORCE_RESTORE</b></dt>
<dt>0x00000008L</dt>
</dl>
</td>
<td width="60%">
If specified, the restore operation is executed even if open handles exist at or beneath the location in the registry hierarchy to which the <i>hKey</i> parameter points. 

</td>
</tr>
<tr>
<td width="40%"><a id="REG_WHOLE_HIVE_VOLATILE"></a><a id="reg_whole_hive_volatile"></a><dl>
<dt><b>REG_WHOLE_HIVE_VOLATILE</b></dt>
<dt>0x00000001L</dt>
</dl>
</td>
<td width="60%">
If specified, a new, volatile (memory only) set of registry information, or hive, is created. If REG_WHOLE_HIVE_VOLATILE is specified, the key identified by the <i>hKey</i> parameter must be either the <b>HKEY_USERS</b> or <b>HKEY_LOCAL_MACHINE</b> value.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



There are two different registry hive file formats. Registry hives created on current operating systems typically cannot be loaded by earlier ones.

If any subkeys of the <i>hKey</i> parameter are open, 
<b>RegRestoreKey</b> fails.

The calling process must have the SE_RESTORE_NAME and SE_BACKUP_NAME privileges on the computer in which the registry resides. For more information, see 
<a href="https://msdn.microsoft.com/b25db548-d5ab-4276-9b50-36d030909384">Running with Special Privileges</a>.

This function replaces the keys and values below the specified key with the keys and values that are subsidiary to the top-level key in the file, no matter what the name of the top-level key in the file might be. For example, <i>hKey</i> might identify a key A with subkeys B and C, while the <i>lpFile</i> parameter specifies a file containing key X with subkeys Y and Z. After a call to 
<b>RegRestoreKey</b>, the registry would contain key A with subkeys Y and Z. The value entries of A would be replaced by the value entries of X.

The new information in the file specified by <i>lpFile</i> overwrites the contents of the key specified by the <i>hKey</i> parameter, except for the key name.

If <i>hKey</i> represents a key in a remote computer, the path described by <i>lpFile</i> is relative to the remote computer.




## -see-also




<a href="https://msdn.microsoft.com/a2310ca0-1b9f-48d1-a3b5-ea3a528bfaba">RegDeleteKey</a>



<a href="https://msdn.microsoft.com/536395aa-03ba-430d-a66d-fcabdc9dfe22">RegLoadKey</a>



<a href="https://msdn.microsoft.com/f968fa71-edc8-4f49-b9fa-1e89224df33b">RegReplaceKey</a>



<a href="https://msdn.microsoft.com/da80f40d-0099-4748-94ca-5d3b001e633e">RegSaveKey</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/ffb06903-593e-47ce-adb2-baed5d379110">Registry Overview</a>
 

 

