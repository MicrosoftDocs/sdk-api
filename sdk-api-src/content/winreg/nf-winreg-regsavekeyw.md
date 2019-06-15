---
UID: NF:winreg.RegSaveKeyW
title: RegSaveKeyW function (winreg.h)
author: windows-sdk-content
description: Saves the specified key and all of its subkeys and values to a new file, in the standard format.
old-location: base\regsavekey.htm
tech.root: SysInfo
ms.assetid: da80f40d-0099-4748-94ca-5d3b001e633e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RegSaveKey, RegSaveKey function, RegSaveKeyA, RegSaveKeyW, _win32_regsavekey, base.regsavekey, winreg/RegSaveKey, winreg/RegSaveKeyA, winreg/RegSaveKeyW
ms.topic: function
f1_keywords: ["winreg/RegSaveKey"]
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
 - RegSaveKey
 - RegSaveKeyA
 - RegSaveKeyW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RegSaveKeyW function


## -description


Saves the specified key and all of its subkeys and values to a new file, in the standard format.

To specify the format for the saved key or hive, use the   <a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regsavekeyexa">RegSaveKeyEx</a> function.

 Applications that back up or restore system state including system files and registry hives should use the <a href="http://go.microsoft.com/fwlink/p/?linkid=177790">Volume Shadow Copy Service</a> instead of the registry functions.


## -parameters




### -param hKey [in]

A handle to an open registry key. 

This handle is returned by the 
<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a> or 
<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a> function, or it can be one of the following 
<a href="https://docs.microsoft.com/windows/desktop/SysInfo/predefined-keys">predefined keys</a>: 


<dl>
<dd><b>HKEY_CLASSES_ROOT</b></dd>
<dd><b>HKEY_CURRENT_USER</b></dd>
</dl>



### -param lpFile [in]

The name of the file in which the specified key and subkeys are to be saved. If the file already exists, the function fails. 




If the string does not include a path, the file is created in the current directory of the calling process for a local key, or in the %systemroot%\system32 directory for a remote key. The new file has the archive attribute.


### -param lpSecurityAttributes [in, optional]

A pointer to a 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)">SECURITY_ATTRIBUTES</a> structure that specifies a security descriptor for the new file. If <i>lpSecurityAttributes</i> is <b>NULL</b>, the file gets a default security descriptor. The ACLs in a default security descriptor for a file are inherited from its parent directory.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.

If the file already exists, the function fails with the ERROR_ALREADY_EXISTS error.




## -remarks



If <i>hKey</i> represents a key on a remote computer, the path described by <i>lpFile</i> is relative to the remote computer.

The 
<b>RegSaveKey</b> function saves only nonvolatile keys. It does not save volatile keys. A key is made volatile or nonvolatile at its creation; see 
<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>.

You can use the file created by 
<b>RegSaveKey</b> in subsequent calls to the 
<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regloadkeya">RegLoadKey</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regreplacekeya">RegReplaceKey</a>, or 
<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regrestorekeya">RegRestoreKey</a> functions. If 
<b>RegSaveKey</b> fails part way through its operation, the file will be corrupt and subsequent calls to 
<b>RegLoadKey</b>, 
<b>RegReplaceKey</b>, or 
<b>RegRestoreKey</b> for the file will fail.

Using <b>RegSaveKey</b> together with 
<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regrestorekeya">RegRestoreKey</a> to copy subtrees in the registry is not recommended. This method does not trigger notifications and can invalidate handles used by other applications. Instead, use the 
<a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-shcopykeya">SHCopyKey</a> function or the <a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regcopytreea">RegCopyTree</a> function.

The calling process must have the SE_BACKUP_NAME privilege enabled. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regdeletekeya">RegDeleteKey</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regloadkeya">RegLoadKey</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regreplacekeya">RegReplaceKey</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regrestorekeya">RegRestoreKey</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regsavekeyexa">RegSaveKeyEx</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/registry-files">Registry Files</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)">SECURITY_ATTRIBUTES</a>
 

 

