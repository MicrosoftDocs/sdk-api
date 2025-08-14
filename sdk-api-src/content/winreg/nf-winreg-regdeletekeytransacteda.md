---
UID: NF:winreg.RegDeleteKeyTransactedA
title: RegDeleteKeyTransactedA function (winreg.h)
description: Deletes a subkey and its values from the specified platform-specific view of the registry as a transacted operation. (ANSI)
helpviewer_keywords: ["KEY_WOW64_32KEY", "KEY_WOW64_64KEY", "RegDeleteKeyTransactedA", "winreg/RegDeleteKeyTransactedA"]
old-location: base\regdeletekeytransacted.htm
tech.root: winprog
ms.assetid: 4c67e08b-4338-4441-8300-6b6ed31d4b21
ms.date: 12/05/2018
ms.keywords: KEY_WOW64_32KEY, KEY_WOW64_64KEY, RegDeleteKeyTransacted, RegDeleteKeyTransacted function, RegDeleteKeyTransactedA, RegDeleteKeyTransactedW, base.regdeletekeytransacted, winreg/RegDeleteKeyTransacted, winreg/RegDeleteKeyTransactedA, winreg/RegDeleteKeyTransactedW
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegDeleteKeyTransactedW (Unicode) and RegDeleteKeyTransactedA (ANSI)
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
 - RegDeleteKeyTransactedA
 - winreg/RegDeleteKeyTransactedA
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
 - RegDeleteKeyTransacted
 - RegDeleteKeyTransactedA
 - RegDeleteKeyTransactedW
---

# RegDeleteKeyTransactedA function


## -description

Deletes a subkey and its values from the specified platform-specific view of the registry as a transacted operation. Note that key names are not case sensitive.

## -parameters

### -param hKey [in]

A handle to an open registry key. The access rights of this key do not affect the delete operation. For more information about access rights, see 
<a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.

This handle is returned by the 
<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>, <a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeytransacteda">RegCreateKeyTransacted</a>, <a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>, or 
<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeytransacteda">RegOpenKeyTransacted</a> function. It can also be one of the following 
<a href="/windows/desktop/SysInfo/predefined-keys">predefined keys</a>:<dl>
<dd><b>HKEY_CLASSES_ROOT</b></dd>
<dd><b>HKEY_CURRENT_CONFIG</b></dd>
<dd><b>HKEY_CURRENT_USER</b></dd>
<dd><b>HKEY_LOCAL_MACHINE</b></dd>
<dd><b>HKEY_USERS</b></dd>
</dl>

### -param lpSubKey [in]

The name of the key to be deleted. This key must be a subkey of the key specified by the value of the <i>hKey</i> parameter. 

The  function opens the subkey with the DELETE access right. 

Key names are not case sensitive.

The value of this parameter cannot be <b>NULL</b>.

### -param samDesired [in]

An access mask the specifies the platform-specific view of the registry.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KEY_WOW64_32KEY"></a><a id="key_wow64_32key"></a><dl>
<dt><b>KEY_WOW64_32KEY</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
Delete the key from the 32-bit registry view.

</td>
</tr>
<tr>
<td width="40%"><a id="KEY_WOW64_64KEY"></a><a id="key_wow64_64key"></a><dl>
<dt><b>KEY_WOW64_64KEY</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
Delete the key from the 64-bit registry view.

</td>
</tr>
</table>

### -param Reserved

This parameter is reserved and must be zero.

### -param hTransaction [in]

A handle to an active transaction. This handle is returned by the <a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a> function.

### -param pExtendedParameter

This parameter is reserved and must be <b>NULL</b>.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.

## -remarks

A deleted key is not removed until the last handle to it is closed.

On WOW64, 32-bit applications view a registry tree that is separate from the registry tree that 64-bit applications view. This function enables an application to delete an entry in the alternate registry view.

The subkey to be deleted must not have subkeys. To delete a key and all its subkeys, you need to enumerate the subkeys and delete them individually. To delete keys recursively, use the 
<a href="/windows/desktop/api/winreg/nf-winreg-regdeletetreea">RegDeleteTree</a> or <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shdeletekeya">SHDeleteKey</a> function.

If the function succeeds, <b>RegDeleteKeyTransacted</b> removes the specified key from the registry. The entire key, including all of its values, is removed. To remove the entire tree as a transacted operation, use the <a href="/windows/desktop/api/winreg/nf-winreg-regdeletetreea">RegDeleteTree</a> function with a handle returned from <a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeytransacteda">RegCreateKeyTransacted</a> or <a href="/windows/desktop/api/winreg/nf-winreg-regopenkeytransacteda">RegOpenKeyTransacted</a>.





> [!NOTE]
> The winreg.h header defines RegDeleteKeyTransacted as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeytransacteda">RegCreateKeyTransacted</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeytransacteda">RegOpenKeyTransacted</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="/windows/desktop/WinProg64/registry-redirector">Registry Redirector</a>
