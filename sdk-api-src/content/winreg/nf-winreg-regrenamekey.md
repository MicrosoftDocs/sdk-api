---
UID: NF:winreg.RegRenameKey
tech.root: winprog
title: RegRenameKey
ms.date: 03/15/2021
targetos: Windows
description: Changes the name of the specified registry key.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.header: winreg.h
req.idl: 
req.include-header: Windows.h
req.irql: 
req.kmdf-ver: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - winreg.h
api_name:
 - RegRenameKey
f1_keywords:
 - RegRenameKey
 - winreg/RegRenameKey
dev_langs:
 - c++
---

## -description

Changes the name of the specified registry key.

## -parameters

### -param hKey

A handle to the key to be renamed. The handle must be opened with the KEY_WRITE access right. For more information, see [Registry Key Security and Access Rights](/windows/win32/SysInfo/registry-key-security-and-access-rights).

This handle is returned by the [RegCreateKeyEx](nf-winreg-regcreatekeyexa.md) or [RegOpenKeyEx](nf-winreg-regopenkeyexa.md) function, or it can be one of the following [Predefined Keys](/windows/win32/SysInfo/predefined-keys):

* HKEY_CLASSES_ROOT
* HKEY_CURRENT_CONFIG
* HKEY_CURRENT_USER
* HKEY_LOCAL_MACHINE
* HKEY_USERS

### -param lpSubKeyName

The name of the subkey to be renamed. This key must be a subkey of the key identified by the *hKey* parameter. This parameter can also be **NULL**, in which case the key identified by the *hKey* parameter will be renamed.

### -param lpNewKeyName

The new name of the key. The new name must not already exist.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the [FormatMessage](/windows/desktop/api/winbase/nf-winbase-formatmessage) function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error. An error code of STATUS_ACCESS_DENIED indicates that the caller does not have the necessary access rights to the specified registry key or subkeys.

## -remarks

This function can be used to rename an entire registry subtree. The caller must have KEY_CREATE_SUB_KEY access to the parent of the specified key and DELETE access to the entire subtree being renamed.

## -see-also

<a href="/windows/win32/api/winreg/nf-winreg-regcopytreew">RegCopyTree</a>

<a href="/windows/win32/SysInfo/registry-functions">Registry Functions</a>

<a href="/windows/win32/SysInfo/registry">Registry Overview</a>

<a href="/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)">SECURITY_ATTRIBUTES</a>
