---
UID: NF:wincred.CredEnumerateW
title: CredEnumerateW function (wincred.h)
description: Enumerates the credentials from the user's credential set. (Unicode)
helpviewer_keywords: ["CRED_ENUMERATE_ALL_CREDENTIALS", "CredEnumerate", "CredEnumerate function [Security]", "CredEnumerateW", "_cred_credenumerate", "security.credenumerate", "wincred/CredEnumerate", "wincred/CredEnumerateW"]
old-location: security\credenumerate.htm
tech.root: security
ms.assetid: ef0b7620-7b00-45f1-af16-141d2e940783
ms.date: 12/05/2018
ms.keywords: CRED_ENUMERATE_ALL_CREDENTIALS, CredEnumerate, CredEnumerate function [Security], CredEnumerateA, CredEnumerateW, _cred_credenumerate, security.credenumerate, wincred/CredEnumerate, wincred/CredEnumerateA, wincred/CredEnumerateW
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CredEnumerateW (Unicode) and CredEnumerateA (ANSI)
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
 - CredEnumerateW
 - wincred/CredEnumerateW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-0.dll
 - sechost.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - API-MS-Win-Security-credentials-l1-1-0.dll
api_name:
 - CredEnumerate
 - CredEnumerateA
 - CredEnumerateW
---

# CredEnumerateW function


## -description

The <b>CredEnumerate</b> function enumerates the credentials from the user's credential set. The credential set used is the one associated with the logon session of the current token. The token must not have the user's SID disabled.

## -parameters

### -param Filter [in]

Pointer to a <b>null</b>-terminated string that contains the filter for the returned credentials. Only credentials with a <i>TargetName</i> matching the filter will be returned. The filter specifies a name prefix followed by an asterisk. For instance, the filter "FRED*" will return all credentials with a <i>TargetName</i> beginning with the string "FRED".


If <b>NULL</b> is specified, all credentials will be returned.

### -param Flags [in]

The value of this parameter can be zero or more of the following values combined with a bitwise-<b>OR</b> operation.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRED_ENUMERATE_ALL_CREDENTIALS"></a><a id="cred_enumerate_all_credentials"></a><dl>
<dt><b>CRED_ENUMERATE_ALL_CREDENTIALS</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
This function enumerates all of the credentials in the user's credential set. The target name of each credential is returned in the "namespace:attribute=target" format. If this flag is set and the <i>Filter</i> parameter is not <b>NULL</b>, the function fails and returns <b>ERROR_INVALID_FLAGS</b>.

<b>Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
</table>

### -param Count [out]

Count of the credentials returned in the <i>Credentials</i> array.

### -param Credential [out]

Pointer to an array of pointers to credentials.
The returned credential is a single allocated block. Any pointers contained within the buffer are pointers to locations within this single allocated block. The single returned buffer must be freed by calling <a href="/windows/desktop/api/wincred/nf-wincred-credfree">CredFree</a>.

## -returns

The function returns <b>TRUE</b> on success and <b>FALSE</b> on failure. The <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function can be called to get a more specific status code. The following status codes can be returned.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
<dt>1168 (0x490)</dt>
</dl>
</td>
<td width="60%">
No credential exists matching the specified <i>Filter</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_LOGON_SESSION</b></dt>
<dt>1312 (0x520)</dt>
</dl>
</td>
<td width="60%">
The logon session does not exist or there is no credential set associated with this logon session. Network logon sessions do not have an associated credential set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FLAGS</b></dt>
<dt>1004 (0x3EC)</dt>
</dl>
</td>
<td width="60%">
A flag that is not valid was specified for the <i>Flags</i> parameter, or <b>CRED_ENUMERATE_ALL_CREDENTIALS</b> is specified for the <i>Flags</i> parameter and the <i>Filter</i> parameter is not <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wincred/nf-wincred-credfree">CredFree</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>

## -remarks

> [!NOTE]
> The wincred.h header defines CredEnumerate as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
