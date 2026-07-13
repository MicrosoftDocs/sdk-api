---
UID: NF:winbase.LogonUserExW
title: LogonUserExW function (winbase.h)
description: The LogonUserEx function attempts to log a user on to the local computer. (Unicode)
helpviewer_keywords: ["LOGON32_LOGON_BATCH", "LOGON32_LOGON_INTERACTIVE", "LOGON32_LOGON_NETWORK", "LOGON32_LOGON_NETWORK_CLEARTEXT", "LOGON32_LOGON_NEW_CREDENTIALS", "LOGON32_LOGON_SERVICE", "LOGON32_LOGON_UNLOCK", "LOGON32_PROVIDER_DEFAULT", "LOGON32_PROVIDER_WINNT40", "LOGON32_PROVIDER_WINNT50", "LogonUserEx", "LogonUserEx function [Security]", "LogonUserExW", "_win32_logonuserex", "security.logonuserex", "winbase/LogonUserEx", "winbase/LogonUserExW"]
old-location: security\logonuserex.htm
tech.root: security
ms.assetid: 4aba1cad-f234-4329-8599-7438cb9bee98
ms.date: 12/05/2018
ms.keywords: LOGON32_LOGON_BATCH, LOGON32_LOGON_INTERACTIVE, LOGON32_LOGON_NETWORK, LOGON32_LOGON_NETWORK_CLEARTEXT, LOGON32_LOGON_NEW_CREDENTIALS, LOGON32_LOGON_SERVICE, LOGON32_LOGON_UNLOCK, LOGON32_PROVIDER_DEFAULT, LOGON32_PROVIDER_WINNT40, LOGON32_PROVIDER_WINNT50, LogonUserEx, LogonUserEx function [Security], LogonUserExA, LogonUserExW, _win32_logonuserex, security.logonuserex, winbase/LogonUserEx, winbase/LogonUserExA, winbase/LogonUserExW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LogonUserExW (Unicode) and LogonUserExA (ANSI)
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
 - LogonUserExW
 - winbase/LogonUserExW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-security-logon-l1-1-0.dll
 - advapi32legacy.dll
 - API-MS-Win-Security-Logon-L1-1-1.dll
api_name:
 - LogonUserEx
 - LogonUserExA
 - LogonUserExW
---

# LogonUserExW function


## -description

The <b>LogonUserEx</b> function attempts to log a user on to the local computer. The local computer is the computer from which <b>LogonUserEx</b> was called. You cannot use <b>LogonUserEx</b> to log on to a remote computer. You specify the user with a user name and domain and <a href="/windows/desktop/SecGloss/a-gly">authenticate</a> the user with a plaintext password. If the function succeeds, you receive a handle to a token that represents the logged-on user. You can then use this token handle to impersonate the specified user or, in most cases, to create a <a href="/windows/desktop/SecGloss/p-gly">process</a>  that runs in the context of the specified user.

## -parameters

### -param lpszUsername [in]

A pointer to a null-terminated string that specifies the name of the user. This is the name of the user account to log on to. If you use the <a href="/windows/desktop/SecGloss/u-gly">user principal name</a> (UPN) format, user@DNS_domain_name, the <i>lpszDomain</i> parameter must be <b>NULL</b>.

### -param lpszDomain [in, optional]

A pointer to a null-terminated string that specifies the name of the domain or server whose account database contains the <i>lpszUsername</i> account. If this parameter is <b>NULL</b>, the user name must be specified in UPN format. If this parameter is ".", the function validates the account by using only the local account database.

### -param lpszPassword [in, optional]

A pointer to a null-terminated string that specifies the plaintext password for the user account specified by <i>lpszUsername</i>.  When you have finished using the password, clear the password from memory by calling the <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> function. For more information about protecting passwords, see <a href="/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.

### -param dwLogonType [in]

The type of logon operation to perform. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LOGON32_LOGON_BATCH"></a><a id="logon32_logon_batch"></a><dl>
<dt><b>LOGON32_LOGON_BATCH</b></dt>
</dl>
</td>
<td width="60%">
This logon type is intended for batch servers, where processes may be executing on behalf of a user without their direct intervention. This type is also for higher performance servers that process many plaintext authentication attempts at a time, such as mail or web servers. The <b>LogonUserEx</b> function does not cache credentials for this logon type.

</td>
</tr>
<tr>
<td width="40%"><a id="LOGON32_LOGON_INTERACTIVE"></a><a id="logon32_logon_interactive"></a><dl>
<dt><b>LOGON32_LOGON_INTERACTIVE</b></dt>
</dl>
</td>
<td width="60%">
This logon type is intended for users who will be interactively using the computer, such as a user being logged on by a <a href="/windows/desktop/SecGloss/t-gly">terminal</a> server, remote shell, or similar process. This logon type has the additional expense of caching logon information for disconnected operations; therefore, it is inappropriate for some client/server applications, such as a mail server.

</td>
</tr>
<tr>
<td width="40%"><a id="LOGON32_LOGON_NETWORK"></a><a id="logon32_logon_network"></a><dl>
<dt><b>LOGON32_LOGON_NETWORK</b></dt>
</dl>
</td>
<td width="60%">
This logon type is intended for high performance servers to authenticate plaintext passwords. The <b>LogonUserEx</b> function does not cache credentials for this logon type.

</td>
</tr>
<tr>
<td width="40%"><a id="LOGON32_LOGON_NETWORK_CLEARTEXT"></a><a id="logon32_logon_network_cleartext"></a><dl>
<dt><b>LOGON32_LOGON_NETWORK_CLEARTEXT</b></dt>
</dl>
</td>
<td width="60%">
This logon type preserves the name and password in the <a href="/windows/desktop/SecGloss/a-gly">authentication package</a>, which allows the server to make connections to other network servers while impersonating the client. A server can accept plaintext credentials from a client, call <b>LogonUserEx</b>, verify that the user can access the system across the network, and still communicate with other servers.
							

</td>
</tr>
<tr>
<td width="40%"><a id="LOGON32_LOGON_NEW_CREDENTIALS"></a><a id="logon32_logon_new_credentials"></a><dl>
<dt><b>LOGON32_LOGON_NEW_CREDENTIALS</b></dt>
</dl>
</td>
<td width="60%">
This logon type allows the caller to clone its current token and specify new credentials for outbound connections. The new logon session has the same local identifier but uses different credentials for other network connections.

This logon type is supported only by the LOGON32_PROVIDER_WINNT50 logon provider.

</td>
</tr>
<tr>
<td width="40%"><a id="LOGON32_LOGON_SERVICE"></a><a id="logon32_logon_service"></a><dl>
<dt><b>LOGON32_LOGON_SERVICE</b></dt>
</dl>
</td>
<td width="60%">
Indicates a service-type logon. The account provided must have the service privilege enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="LOGON32_LOGON_UNLOCK"></a><a id="logon32_logon_unlock"></a><dl>
<dt><b>LOGON32_LOGON_UNLOCK</b></dt>
</dl>
</td>
<td width="60%">
This logon type is for <a href="/windows/desktop/SecGloss/g-gly">GINA</a> DLLs that log on users who will be interactively using the computer. This logon type can generate a unique audit record that shows when the workstation was unlocked.

</td>
</tr>
</table>

### -param dwLogonProvider [in]

The logon provider. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LOGON32_PROVIDER_DEFAULT"></a><a id="logon32_provider_default"></a><dl>
<dt><b>LOGON32_PROVIDER_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Use the standard logon provider for the system. The default <a href="/windows/desktop/SecGloss/s-gly">security provider</a> is NTLM.

</td>
</tr>
<tr>
<td width="40%"><a id="LOGON32_PROVIDER_WINNT50"></a><a id="logon32_provider_winnt50"></a><dl>
<dt><b>LOGON32_PROVIDER_WINNT50</b></dt>
</dl>
</td>
<td width="60%">
Use the negotiate logon provider.
							

</td>
</tr>
<tr>
<td width="40%"><a id="LOGON32_PROVIDER_WINNT40"></a><a id="logon32_provider_winnt40"></a><dl>
<dt><b>LOGON32_PROVIDER_WINNT40</b></dt>
</dl>
</td>
<td width="60%">
Use the NTLM logon provider.

</td>
</tr>
</table>

### -param phToken [out, optional]

A pointer to a handle variable that receives a handle to a token that represents the specified user.

You can use the returned handle in calls to the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser">ImpersonateLoggedOnUser</a> function.

In most cases, the returned handle is a <a href="/windows/desktop/SecGloss/p-gly">primary token</a> that you can use in calls to the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a> function. However, if you specify the LOGON32_LOGON_NETWORK flag, <b>LogonUserEx</b> returns an <a href="/windows/desktop/SecGloss/i-gly">impersonation token</a> that you cannot use in <b>CreateProcessAsUser</b> unless you call <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex">DuplicateTokenEx</a> to convert the impersonation token to a primary token.

When you no longer need this handle, close it by calling the 
<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function.

### -param ppLogonSid [out, optional]

A pointer to a pointer to a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) that receives the SID of the user logged on.

When you have finished using the SID, free it by calling the <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function.

### -param ppProfileBuffer [out, optional]

A pointer to a pointer that receives the address of a buffer that contains the logged on user's profile.

### -param pdwProfileLength [out, optional]

A pointer to a <b>DWORD</b> that receives the length of the profile buffer.

### -param pQuotaLimits [out, optional]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-quota_limits">QUOTA_LIMITS</a> structure that receives information about the quotas for the logged on user.

## -returns

If the function succeeds, the function returns  nonzero.

If the function fails, it returns  zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The LOGON32_LOGON_NETWORK logon type is fastest, but it has the following limitations:

<ul>
<li>The function returns an <a href="/windows/desktop/SecGloss/i-gly">impersonation token</a>, not a primary token. You cannot use this token directly in the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a> function. However, you can call the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex">DuplicateTokenEx</a> function to convert the token to a primary token, and then use it in <b>CreateProcessAsUser</b>.</li>
<li>If you convert the token to a primary token and use it in <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a> to start a process, the new process cannot access other network resources, such as remote servers or printers, through the redirector. An exception is that if the network resource is not access controlled, then the new process will be able to access it.</li>
</ul>


The SE_TCB_NAME privilege is not required for this function unless you are logging onto a Passport account.

The account specified by <i>lpszUsername</i> must have the necessary account rights. For example, to log on a user with the LOGON32_LOGON_INTERACTIVE flag, the user (or a group to which the user belongs) must have the SE_INTERACTIVE_LOGON_NAME account right. For a list of the account rights that affect the various logon operations, see 
<a href="/windows/desktop/SecMgmt/account-object-access-rights">Account Object Access Rights</a>.

A user is considered logged on if at least one token exists. If you call 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a> and then close the token, the user is still logged on until the process (and all child processes) have ended.

If the <b>LogonUserEx</b> call is successful, the system notifies network providers that the logon occurred by calling the provider's <a href="/windows/desktop/api/npapi/nf-npapi-nplogonnotify">NPLogonNotify</a> entry-point function.





> [!NOTE]
> The winbase.h header defines LogonUserEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SecAuthZ/client-server-access-control">Client/Server Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Client/Server Access Control Functions</a>



<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex">DuplicateTokenEx</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser">ImpersonateLoggedOnUser</a>



<a href="/windows/desktop/api/winnt/ns-winnt-quota_limits">QUOTA_LIMITS</a>
