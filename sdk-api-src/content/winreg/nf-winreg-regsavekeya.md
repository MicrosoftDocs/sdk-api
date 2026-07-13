---
UID: NF:winreg.RegSaveKeyA
title: RegSaveKeyA function (winreg.h)
description: Saves the specified key and all of its subkeys and values to a new file, in the standard format. (ANSI)
helpviewer_keywords: ["RegSaveKeyA", "winreg/RegSaveKeyA"]
old-location: base\regsavekey.htm
tech.root: winprog
ms.assetid: da80f40d-0099-4748-94ca-5d3b001e633e
ms.date: 12/05/2018
ms.keywords: RegSaveKey, RegSaveKey function, RegSaveKeyA, RegSaveKeyW, _win32_regsavekey, base.regsavekey, winreg/RegSaveKey, winreg/RegSaveKeyA, winreg/RegSaveKeyW
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegSaveKeyW (Unicode) and RegSaveKeyA (ANSI)
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
 - RegSaveKeyA
 - winreg/RegSaveKeyA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-registry-l2-3-0.dll
 - Advapi32.dll
 - API-MS-Win-Core-Registry-l2-1-0.dll
 - advapi32legacy.dll
 - API-MS-Win-Core-Registry-l2-2-0.dll
api_name:
 - RegSaveKey
 - RegSaveKeyA
 - RegSaveKeyW
---

# RegSaveKeyA function


## -description

Saves the specified key and all of its subkeys and values to a new file, in the standard format.

To specify the format for the saved key or hive, use the   <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeyexa">RegSaveKeyEx</a> function.

 Applications that back up or restore system state including system files and registry hives should use the <a href="/windows/win32/vss/volume-shadow-copy-service-overview">Volume Shadow Copy Service</a> instead of the registry functions.

## -parameters

### -param hKey [in]

A handle to an open registry key. 

This handle is returned by the 
<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a> or 
<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a> function, or it can be one of the following 
<a href="/windows/desktop/SysInfo/predefined-keys">predefined keys</a>: 


<dl>
<dd><b>HKEY_CLASSES_ROOT</b></dd>
<dd><b>HKEY_CURRENT_USER</b></dd>
</dl>

### -param lpFile [in]

The name of the file in which the specified key and subkeys are to be saved. If the file already exists, the function fails. 




If the string does not include a path, the file is created in the current directory of the calling process for a local key, or in the %systemroot%\system32 directory for a remote key. The new file has the archive attribute.

### -param lpSecurityAttributes [in, optional]

A pointer to a 
<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure that specifies a security descriptor for the new file. If <i>lpSecurityAttributes</i> is <b>NULL</b>, the file gets a default security descriptor. The ACLs in a default security descriptor for a file are inherited from its parent directory.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.

If the file already exists, the function fails with the ERROR_ALREADY_EXISTS error.

## -remarks

If <i>hKey</i> represents a key on a remote computer, the path described by <i>lpFile</i> is relative to the remote computer.

The 
<b>RegSaveKey</b> function saves only nonvolatile keys. It does not save volatile keys. A key is made volatile or nonvolatile at its creation; see 
<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>.

You can use the file created by 
<b>RegSaveKey</b> in subsequent calls to the 
<a href="/windows/desktop/api/winreg/nf-winreg-regloadkeya">RegLoadKey</a>, 
<a href="/windows/desktop/api/winreg/nf-winreg-regreplacekeya">RegReplaceKey</a>, or 
<a href="/windows/desktop/api/winreg/nf-winreg-regrestorekeya">RegRestoreKey</a> functions. If 
<b>RegSaveKey</b> fails part way through its operation, the file will be corrupt and subsequent calls to 
<b>RegLoadKey</b>, 
<b>RegReplaceKey</b>, or 
<b>RegRestoreKey</b> for the file will fail.

Using <b>RegSaveKey</b> together with 
<a href="/windows/desktop/api/winreg/nf-winreg-regrestorekeya">RegRestoreKey</a> to copy subtrees in the registry is not recommended. This method does not trigger notifications and can invalidate handles used by other applications. Instead, use the 
<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shcopykeya">SHCopyKey</a> function or the <a href="/windows/desktop/api/winreg/nf-winreg-regcopytreea">RegCopyTree</a> function.

The calling process must have the SE_BACKUP_NAME privilege enabled. For more information, see 
<a href="/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>.





> [!NOTE]
> The winreg.h header defines RegSaveKey as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regdeletekeya">RegDeleteKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regloadkeya">RegLoadKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regreplacekeya">RegReplaceKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regrestorekeya">RegRestoreKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regsavekeyexa">RegSaveKeyEx</a>



<a href="/windows/desktop/SysInfo/registry-files">Registry Files</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a>
