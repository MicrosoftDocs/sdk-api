---
UID: NF:winreg.RegRenameKey
title: RegRenameKey function (winreg.h)
description: Renames the specified registry key. Note that key names are not case sensitive.
helpviewer_keywords: ["RegRenameKey","RegRenameKey function","_win32_regrenamekey","base.regrenamekey","winreg/RegRenameKey"]
old-location: base\regrenamekey.htm
tech.root: winprog
ms.assetid: 41a91ec8-b5b0-44ee-bea8-8536acb3db69
ms.date: 03/14/2021
ms.keywords: RegRenameKey, RegRenameKey function, _win32_regrenamekey, base.regrenamekey, winreg/RegRenameKey
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi:
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
 - RegRenameKey
 - winreg/RegRenameKey
dev_langs:
 - c++
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
 - RegRenameKey
---

# RegRenameKey function


## -description

Renames the specified registry key. Note that key names are not case sensitive.

## -parameters

### -param hKey [in]

A handle to an open registry key. The calling process must have KEY_WRITE access to the key. For more information, see 
<a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.

This handle is returned by the 
<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a> or 
<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a> function, or it can be one of the following 
<a href="/windows/desktop/SysInfo/predefined-keys">Predefined Keys</a>:<dl>
<dd><b>HKEY_CLASSES_ROOT</b></dd>
<dd><b>HKEY_CURRENT_CONFIG</b></dd>
<dd><b>HKEY_CURRENT_USER</b></dd>
<dd><b>HKEY_LOCAL_MACHINE</b></dd>
<dd><b>HKEY_USERS</b></dd>
</dl>

### -param lpSubKey [in, optional]

The name of the key to be renamed. This key must be a subkey of the key identified by the <i>hKeySrc</i> parameter. This parameter can also be <b>NULL</b>, in which case the key identified by the <i>hKeySrc</i> parameter will be renamed.

### -param lpSubKeyDest [in]

The new name of the key. The new name must not already exist.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regcopytreew">RegCopyTree</a>

<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>

<a href="/windows/desktop/SysInfo/registry">Registry Overview</a>

<a href="/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)">SECURITY_ATTRIBUTES</a>
