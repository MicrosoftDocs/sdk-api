---
UID: NF:winsafer.SaferComputeTokenFromLevel
title: SaferComputeTokenFromLevel function (winsafer.h)
description: Restricts a token using restrictions specified by a SAFER_LEVEL_HANDLE.
helpviewer_keywords: ["SAFER_TOKEN_COMPARE_ONLY","SAFER_TOKEN_MAKE_INERT","SAFER_TOKEN_NULL_IF_EQUAL","SAFER_TOKEN_WANT_FLAGS","SaferComputeTokenFromLevel","SaferComputeTokenFromLevel function [Security]","security.safercomputetokenfromlevel","winsafer/SaferComputeTokenFromLevel"]
old-location: security\safercomputetokenfromlevel.htm
tech.root: security
ms.assetid: 39406331-3101-48f2-8b92-e049849b2b38
ms.date: 12/05/2018
ms.keywords: SAFER_TOKEN_COMPARE_ONLY, SAFER_TOKEN_MAKE_INERT, SAFER_TOKEN_NULL_IF_EQUAL, SAFER_TOKEN_WANT_FLAGS, SaferComputeTokenFromLevel, SaferComputeTokenFromLevel function [Security], security.safercomputetokenfromlevel, winsafer/SaferComputeTokenFromLevel
req.header: winsafer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - SaferComputeTokenFromLevel
 - winsafer/SaferComputeTokenFromLevel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - Ext-MS-Win-AdvAPI32-safer-l1-1-0.dll
api_name:
 - SaferComputeTokenFromLevel
req.apiset: ext-ms-win-advapi32-safer-l1-1-0 (introduced in Windows 8)
---

# SaferComputeTokenFromLevel function


## -description

The <b>SaferComputeTokenFromLevel</b> function restricts a token using restrictions specified by a SAFER_LEVEL_HANDLE.

## -parameters

### -param LevelHandle [in]

<b>SAFER_LEVEL_HANDLE</b> that contains the restrictions to place on the input token. Do not pass handles with a LevelId of <b>SAFER_LEVELID_FULLYTRUSTED</b> or <b>SAFER_LEVELID_DISALLOWED</b> to this function. This is because <b>SAFER_LEVELID_FULLYTRUSTED</b> is unrestricted and <b>SAFER_LEVELID_DISALLOWED</b> does not contain a token.

### -param InAccessToken [in, optional]

Token to be restricted. If this parameter is <b>NULL</b>, the token of the current thread will be used. If the current thread does not contain a token, the token of the current process is used.

### -param OutAccessToken [out]

The resulting restricted token.

### -param dwFlags [in]

Specifies the behavior of the method. The value can be <b>NULL</b> or one or more of the following values  combined by using a bitwise-<b>OR</b> operation.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SAFER_TOKEN_NULL_IF_EQUAL"></a><a id="safer_token_null_if_equal"></a><dl>
<dt><b>SAFER_TOKEN_NULL_IF_EQUAL</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
If the <i>OutAccessToken</i> parameter is not more restrictive than the <i>InAccessToken</i> parameter, the <i>OutAccessToken</i> parameter returns <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="SAFER_TOKEN_COMPARE_ONLY"></a><a id="safer_token_compare_only"></a><dl>
<dt><b>SAFER_TOKEN_COMPARE_ONLY</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
The token specified by the <i>InAccessToken</i> parameter is compared with the token that would be created if the restrictions specified by the <i>LevelHandle</i> parameter were applied. The restricted token is not actually created.

On output, the value of the <i>lpReserved</i> parameter specifies the result of the comparison.

</td>
</tr>
<tr>
<td width="40%"><a id="SAFER_TOKEN_MAKE_INERT"></a><a id="safer_token_make_inert"></a><dl>
<dt><b>SAFER_TOKEN_MAKE_INERT</b></dt>
<dt>4 (0x4)</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the system does not check <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd723678(v=ws.10)">AppLocker</a> rules  or apply <a href="/previous-versions/windows/it-pro/windows-server-2003/cc779607(v=ws.10)">Software Restriction Policies</a>. For <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd723678(v=ws.10)">AppLocker</a>, this flag disables checks for all four rule collections: Executable, Windows Installer, Script, and DLL. 

Set this flag when creating a setup program that must run extracted DLLs during installation.

A token can be queried for existence of this flag by using <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>AppLocker is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SAFER_TOKEN_WANT_FLAGS"></a><a id="safer_token_want_flags"></a><dl>
<dt><b>SAFER_TOKEN_WANT_FLAGS</b></dt>
<dt>8 (0x8)</dt>
</dl>
</td>
<td width="60%">
On output, the value of the <i>lpReserved</i> parameter specifies the set of flags used to create the restricted token.

</td>
</tr>
</table>

### -param lpReserved [in, out, optional]

If the <b>SAFER_TOKEN_COMPARE_ONLY</b>  flag is set, this parameter, on output, specifies the result of the token comparison. The output value is an <b>LPDWORD</b>. A value of –1 indicates that the resulting token would be less privileged than the token specified by the <i>InAccessToken</i> parameter.

If the <b>SAFER_TOKEN_WANT_FLAGS</b> flag is set, and the <b>SAFER_TOKEN_COMPARE_ONLY</b> flag is not set, this parameter is an <b>LPDWORD</b> value that specifies the flags used to create the restricted token.

## -returns

<b>TRUE</b> if the function succeeds; otherwise, <b>FALSE</b>. For extended information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.
