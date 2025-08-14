---
UID: NF:winreg.RegSaveKeyExA
title: RegSaveKeyExA function (winreg.h)
description: Saves the specified key and all of its subkeys and values to a registry file, in the specified format. (ANSI)
helpviewer_keywords: ["REG_LATEST_FORMAT", "REG_NO_COMPRESSION", "REG_STANDARD_FORMAT", "RegSaveKeyExA", "winreg/RegSaveKeyExA"]
old-location: base\regsavekeyex.htm
tech.root: winprog
ms.assetid: f93b4162-cac4-42f7-bfd4-9e23fff80a03
ms.date: 12/05/2018
ms.keywords: REG_LATEST_FORMAT, REG_NO_COMPRESSION, REG_STANDARD_FORMAT, RegSaveKeyEx, RegSaveKeyEx function, RegSaveKeyExA, RegSaveKeyExW, _win32_regsavekeyex, base.regsavekeyex, winreg/RegSaveKeyEx, winreg/RegSaveKeyExA, winreg/RegSaveKeyExW
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegSaveKeyExW (Unicode) and RegSaveKeyExA (ANSI)
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
 - RegSaveKeyExA
 - winreg/RegSaveKeyExA
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
 - RegSaveKeyEx
 - RegSaveKeyExA
 - RegSaveKeyExW
---

# RegSaveKeyExA function


## -description

Saves the specified key and all of its subkeys and values to a registry file, in the specified format.

 Applications that back up or restore system state including system files and registry hives should use the <a href="/windows/win32/vss/volume-shadow-copy-service-overview">Volume Shadow Copy Service</a> instead of the registry functions.

## -parameters

### -param hKey [in]

A handle to an open registry key. 

This function does not support the <b>HKEY_CLASSES_ROOT</b> predefined key.

### -param lpFile [in]

The name of the file in which the specified key and subkeys are to be saved. If the file already exists, the function fails. 




The new file has the archive attribute.

If the string does not include a path, the file is created in the current directory of the calling process for a local key, or in the %systemroot%\system32 directory for a remote key.

### -param lpSecurityAttributes [in, optional]

A pointer to a 
<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure that specifies a security descriptor for the new file. If <i>lpSecurityAttributes</i> is <b>NULL</b>, the file gets a default security descriptor. The ACLs in a default security descriptor for a file are inherited from its parent directory.

### -param Flags [in]

The format of the saved key or hive. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="REG_STANDARD_FORMAT"></a><a id="reg_standard_format"></a><dl>
<dt><b>REG_STANDARD_FORMAT</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The key or hive is saved in standard format. The standard format is the only format supported by Windows 2000.

</td>
</tr>
<tr>
<td width="40%"><a id="REG_LATEST_FORMAT"></a><a id="reg_latest_format"></a><dl>
<dt><b>REG_LATEST_FORMAT</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The key or hive is saved in the latest format. The latest format is supported starting with Windows XP. After the key or hive is saved in this format, it cannot be loaded on an earlier system.

</td>
</tr>
<tr>
<td width="40%"><a id="REG_NO_COMPRESSION"></a><a id="reg_no_compression"></a><dl>
<dt><b>REG_NO_COMPRESSION</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The hive is saved with no compression, for faster save operations. The <i>hKey</i> parameter must specify the root of a hive under <b>HKEY_LOCAL_MACHINE </b> or <b>HKEY_USERS</b>. For example, <b>HKLM\SOFTWARE</b> is the root of a hive.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.

If more than one of the possible values listed above for the <i>Flags</i> parameter is specified in one call to this function—for example, if two or more values are OR'ed— or if REG_NO_COMPRESSION is specified and <i>hKey</i> specifies a key that is not the root of a hive, this function returns ERROR_INVALID_PARAMETER.

## -remarks

Unlike <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya">RegSaveKey</a>, this function does not support the <b>HKEY_CLASSES_ROOT</b> predefined key.

If <i>hKey</i> represents a key on a remote computer, the path described by <i>lpFile</i> is relative to the remote computer.

The 
<b>RegSaveKeyEx</b> function saves only nonvolatile keys. It does not save volatile keys. A key is made volatile or nonvolatile at its creation; see 
<b>RegCreateKeyEx</b>.

You can use the file created by 
<b>RegSaveKeyEx</b> in subsequent calls to the 
<a href="/windows/desktop/api/winreg/nf-winreg-regloadkeya">RegLoadKey</a>, 
<a href="/windows/desktop/api/winreg/nf-winreg-regreplacekeya">RegReplaceKey</a>, or 
<a href="/windows/desktop/api/winreg/nf-winreg-regrestorekeya">RegRestoreKey</a> function. If 
<b>RegSaveKeyEx</b> fails partway through its operation, the file will be corrupt and subsequent calls to 
<b>RegLoadKey</b>, 
<b>RegReplaceKey</b>, or 
<b>RegRestoreKey</b> for the file will fail.

Using <b>RegSaveKeyEx</b> together with 
<a href="/windows/desktop/api/winreg/nf-winreg-regrestorekeya">RegRestoreKey</a> to copy subtrees in the registry is not recommended. This method does not trigger notifications and can invalidate handles used by other applications. Instead, use the 
<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shcopykeya">SHCopyKey</a> function or the <a href="/windows/desktop/api/winreg/nf-winreg-regcopytreea">RegCopyTree</a> function.

The calling process must have the SE_BACKUP_NAME privilege enabled. For more information, see 
<a href="/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>.





> [!NOTE]
> The winreg.h header defines RegSaveKeyEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regdeletekeya">RegDeleteKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regloadkeya">RegLoadKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regreplacekeya">RegReplaceKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regrestorekeya">RegRestoreKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya">RegSaveKey</a>



<a href="/windows/desktop/SysInfo/registry-files">Registry Files</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a>
