---
UID: NF:securitybaseapi.DuplicateTokenEx
title: DuplicateTokenEx function (securitybaseapi.h)
description: Creates a new access token that duplicates an existing token. This function can create either a primary token or an impersonation token.
helpviewer_keywords: ["DuplicateTokenEx","DuplicateTokenEx function [Security]","TokenImpersonation","TokenPrimary","_win32_duplicatetokenex","security.duplicatetokenex","securitybaseapi/DuplicateTokenEx"]
old-location: security\duplicatetokenex.htm
tech.root: security
ms.assetid: 96b13826-0ac7-4d70-9c21-eeb343f6b823
ms.date: 12/05/2018
ms.keywords: DuplicateTokenEx, DuplicateTokenEx function [Security], TokenImpersonation, TokenPrimary, _win32_duplicatetokenex, security.duplicatetokenex, securitybaseapi/DuplicateTokenEx
req.header: securitybaseapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - DuplicateTokenEx
 - securitybaseapi/DuplicateTokenEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-base-l1-2-2.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - DuplicateTokenEx
---

# DuplicateTokenEx function


## -description

The <b>DuplicateTokenEx</b> function creates a new <a href="/windows/desktop/SecGloss/a-gly">access token</a> that duplicates an existing token. This function can create either a <a href="/windows/desktop/SecGloss/p-gly">primary token</a> or an <a href="/windows/desktop/SecGloss/i-gly">impersonation token</a>.

## -parameters

### -param hExistingToken [in]

A handle to an access token opened with TOKEN_DUPLICATE access.

### -param dwDesiredAccess [in]

Specifies the requested access rights for the new token. The <b>DuplicateTokenEx</b> function compares the requested access rights with the existing token's <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL) to determine which rights are granted or denied. To request the same access rights as the existing token, specify zero. To request all access rights that are valid for the caller, specify MAXIMUM_ALLOWED. 




For a list of access rights for access tokens, see 
<a href="/windows/desktop/SecAuthZ/access-rights-for-access-token-objects">Access Rights for Access-Token Objects</a>.

### -param lpTokenAttributes [in, optional]

A pointer to a 
<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure that specifies a <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> for the new token and determines whether child processes can inherit the token. If <i>lpTokenAttributes</i> is <b>NULL</b>, the token gets a default security descriptor and the handle cannot be inherited. If the security descriptor contains a <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL), the token gets ACCESS_SYSTEM_SECURITY access right, even if it was not requested in <i>dwDesiredAccess</i>.

To set the owner in the security descriptor for the new token, the caller's process token must have the <b>SE_RESTORE_NAME</b> privilege set.

### -param ImpersonationLevel [in]

Specifies a value from the 
<a href="/windows/desktop/api/winnt/ne-winnt-security_impersonation_level">SECURITY_IMPERSONATION_LEVEL</a> enumeration that indicates the impersonation level of the new token.

### -param TokenType [in]

Specifies one of the following values from the <a href="/windows/desktop/api/winnt/ne-winnt-token_type">TOKEN_TYPE</a> enumeration.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TokenPrimary"></a><a id="tokenprimary"></a><a id="TOKENPRIMARY"></a><dl>
<dt><b>TokenPrimary</b></dt>
</dl>
</td>
<td width="60%">
The new token is a <a href="/windows/desktop/SecGloss/p-gly">primary token</a> that you can use in the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="TokenImpersonation"></a><a id="tokenimpersonation"></a><a id="TOKENIMPERSONATION"></a><dl>
<dt><b>TokenImpersonation</b></dt>
</dl>
</td>
<td width="60%">
The new token is an impersonation token.

</td>
</tr>
</table>

### -param phNewToken [out]

A pointer to a <b>HANDLE</b> variable that receives the new token.

When you have finished using the new token, call the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to close the token handle.

## -returns

If the function succeeds, the function returns a nonzero value.

If the function fails, it returns zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>DuplicateTokenEx</b> function allows you to create a <a href="/windows/desktop/SecGloss/p-gly">primary token</a> that you can use in the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a> function. This allows a server application that is impersonating a client to create a process that has the <a href="/windows/desktop/SecGloss/s-gly">security context</a> of the client. Note that the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetoken">DuplicateToken</a> function can create only impersonation tokens, which are not valid for <b>CreateProcessAsUser</b>.

The following is a typical scenario for using <b>DuplicateTokenEx</b> to create a <a href="/windows/desktop/SecGloss/p-gly">primary token</a>. A server application creates a thread that calls one of the impersonation functions, such as 
<a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient">ImpersonateNamedPipeClient</a>, to impersonate a client. The impersonating thread then calls the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken">OpenThreadToken</a> function to get its own token, which is an <a href="/windows/desktop/SecGloss/i-gly">impersonation token</a> that has the security context of the client. The thread specifies this impersonation token in a call to <b>DuplicateTokenEx</b>, specifying the TokenPrimary flag. The <b>DuplicateTokenEx</b> function creates a <i>primary token</i> that has the security context of the client.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeimpersonateclient">DdeImpersonateClient</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetoken">DuplicateToken</a>



<a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient">ImpersonateNamedPipeClient</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken">OpenThreadToken</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself">RevertToSelf</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient">RpcImpersonateClient</a>



<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a>



<a href="/windows/desktop/api/winnt/ne-winnt-security_impersonation_level">SECURITY_IMPERSONATION_LEVEL</a>