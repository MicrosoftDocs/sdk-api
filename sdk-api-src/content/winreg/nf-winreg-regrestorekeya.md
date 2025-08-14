---
UID: NF:winreg.RegRestoreKeyA
title: RegRestoreKeyA function (winreg.h)
description: Reads the registry information in a specified file and copies it over the specified key. This registry information may be in the form of a key and multiple levels of subkeys. (ANSI)
helpviewer_keywords: ["REG_FORCE_RESTORE", "REG_WHOLE_HIVE_VOLATILE", "RegRestoreKeyA", "winreg/RegRestoreKeyA"]
old-location: base\regrestorekey.htm
tech.root: winprog
ms.assetid: 6267383d-427a-4ae8-b9cc-9c1861d3b7bb
ms.date: 12/05/2018
ms.keywords: REG_FORCE_RESTORE, REG_WHOLE_HIVE_VOLATILE, RegRestoreKey, RegRestoreKey function, RegRestoreKeyA, RegRestoreKeyW, _win32_regrestorekey, base.regrestorekey, winreg/RegRestoreKey, winreg/RegRestoreKeyA, winreg/RegRestoreKeyW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegRestoreKeyA
 - winreg/RegRestoreKeyA
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
 - RegRestoreKey
 - RegRestoreKeyA
 - RegRestoreKeyW
---

# RegRestoreKeyA function


## -description

Reads the registry information in a specified file and copies it over the specified key. This registry information may be in the form of a key and multiple levels of subkeys.

 Applications that back up or restore system state including system files and registry hives should use the <a href="/windows/win32/vss/volume-shadow-copy-service-overview">Volume Shadow Copy Service</a> instead of the registry functions.

## -parameters

### -param hKey [in]

A handle to an open registry key. This handle is returned by the 
<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a> or <a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a> function. It can also be one of the following 
<a href="/windows/desktop/SysInfo/predefined-keys">predefined keys</a>: 




<b>HKEY_CLASSES_ROOT</b>
<b>HKEY_CURRENT_CONFIG</b>
<b>HKEY_CURRENT_USER</b>
<b>HKEY_LOCAL_MACHINE</b>
<b>HKEY_USERS</b>
Any information contained in this key and its descendent keys is overwritten by the information in the file pointed to by the <i>lpFile</i> parameter.

### -param lpFile [in]

The name of the file with the registry information. This file is typically created by using the 
<a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya">RegSaveKey</a> function.

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
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.

## -remarks

There are two different registry hive file formats. Registry hives created on current operating systems typically cannot be loaded by earlier ones.

If any subkeys of the <i>hKey</i> parameter are open, 
<b>RegRestoreKey</b> fails.

The calling process must have the SE_RESTORE_NAME and SE_BACKUP_NAME privileges on the computer in which the registry resides. For more information, see 
<a href="/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>.

This function replaces the keys and values below the specified key with the keys and values that are subsidiary to the top-level key in the file, no matter what the name of the top-level key in the file might be. For example, <i>hKey</i> might identify a key A with subkeys B and C, while the <i>lpFile</i> parameter specifies a file containing key X with subkeys Y and Z. After a call to 
<b>RegRestoreKey</b>, the registry would contain key A with subkeys Y and Z. The value entries of A would be replaced by the value entries of X.

The new information in the file specified by <i>lpFile</i> overwrites the contents of the key specified by the <i>hKey</i> parameter, except for the key name.

If <i>hKey</i> represents a key in a remote computer, the path described by <i>lpFile</i> is relative to the remote computer.





> [!NOTE]
> The winreg.h header defines RegRestoreKey as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regdeletekeya">RegDeleteKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regloadkeya">RegLoadKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regreplacekeya">RegReplaceKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya">RegSaveKey</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="/windows/desktop/SysInfo/registry">Registry Overview</a>
