---
UID: NF:winbase.LogonUserExA
title: LogonUserExA function
author: windows-sdk-content
description: The LogonUserEx function attempts to log a user on to the local computer.
old-location: security\logonuserex.htm
old-project: SecAuthN
ms.assetid: 4aba1cad-f234-4329-8599-7438cb9bee98
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: LOGON32_LOGON_BATCH, LOGON32_LOGON_INTERACTIVE, LOGON32_LOGON_NETWORK, LOGON32_LOGON_NETWORK_CLEARTEXT, LOGON32_LOGON_NEW_CREDENTIALS, LOGON32_LOGON_SERVICE, LOGON32_LOGON_UNLOCK, LOGON32_PROVIDER_DEFAULT, LOGON32_PROVIDER_WINNT40, LOGON32_PROVIDER_WINNT50, LogonUserEx, LogonUserEx function [Security], LogonUserExA, LogonUserExW, _win32_logonuserex, security.logonuserex, winbase/LogonUserEx, winbase/LogonUserExA, winbase/LogonUserExW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: PRIORITY_HINT
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
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# LogonUserExA function


## -description


The <b>LogonUserEx</b> function attempts to log a user on to the local computer. The local computer is the computer from which <b>LogonUserEx</b> was called. You cannot use <b>LogonUserEx</b> to log on to a remote computer. You specify the user with a user name and domain and <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">authenticate</a> the user with a plaintext password. If the function succeeds, you receive a handle to a token that represents the logged-on user. You can then use this token handle to impersonate the specified user or, in most cases, to create a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">process</a>  that runs in the context of the specified user.


## -parameters




### -param lpszUsername [in]

A pointer to a null-terminated string that specifies the name of the user. This is the name of the user account to log on to. If you use the <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">user principal name</a> (UPN) format, user@DNS_domain_name, the <i>lpszDomain</i> parameter must be <b>NULL</b>.


### -param lpszDomain [in, optional]

A pointer to a null-terminated string that specifies the name of the domain or server whose account database contains the <i>lpszUsername</i> account. If this parameter is <b>NULL</b>, the user name must be specified in UPN format. If this parameter is ".", the function validates the account by using only the local account database.


### -param lpszPassword [in, optional]

A pointer to a null-terminated string that specifies the plaintext password for the user account specified by <i>lpszUsername</i>.  When you have finished using the password, clear the password from memory by calling the <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> function. For more information about protecting passwords, see <a href="https://msdn.microsoft.com/1d810f71-9bf5-4c5c-a573-c35081f604cf">Handling Passwords</a>.


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
This logon type is intended for users who will be interactively using the computer, such as a user being logged on by a <a href="https://msdn.microsoft.com/11f2e098-1d1e-473b-90ff-7b86eb923e9f">terminal</a> server, remote shell, or similar process. This logon type has the additional expense of caching logon information for disconnected operations; therefore, it is inappropriate for some client/server applications, such as a mail server.

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
This logon type preserves the name and password in the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">authentication package</a>, which allows the server to make connections to other network servers while impersonating the client. A server can accept plaintext credentials from a client, call <b>LogonUserEx</b>, verify that the user can access the system across the network, and still communicate with other servers.
							

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
This logon type is for <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLLs that log on users who will be interactively using the computer. This logon type can generate a unique audit record that shows when the workstation was unlocked.

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
Use the standard logon provider for the system. The default <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security provider</a> is NTLM.

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
<a href="https://msdn.microsoft.com/cf5c31ae-6749-45c2-888f-697060cc8c75">ImpersonateLoggedOnUser</a> function.

In most cases, the returned handle is a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary token</a> that you can use in calls to the 
<a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a> function. However, if you specify the LOGON32_LOGON_NETWORK flag, <b>LogonUserEx</b> returns an <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation token</a> that you cannot use in <b>CreateProcessAsUser</b> unless you call <a href="https://msdn.microsoft.com/96b13826-0ac7-4d70-9c21-eeb343f6b823">DuplicateTokenEx</a> to convert the impersonation token to a primary token.

When you no longer need this handle, close it by calling the 
<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function.


### -param ppLogonSid [out, optional]

A pointer to a pointer to a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) that receives the SID of the user logged on.

When you have finished using the SID, free it by calling the <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function.


### -param ppProfileBuffer [out, optional]

A pointer to a pointer that receives the address of a buffer that contains the logged on user's profile.


### -param pdwProfileLength [out, optional]

A pointer to a <b>DWORD</b> that receives the length of the profile buffer.


### -param pQuotaLimits [out, optional]

A pointer to a <a href="https://msdn.microsoft.com/7514ec77-34b1-490d-ba21-3b6944942aa7">QUOTA_LIMITS</a> structure that receives information about the quotas for the logged on user.


## -returns



If the function succeeds, the function returns  nonzero.

If the function fails, it returns  zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks




The LOGON32_LOGON_NETWORK logon type is fastest, but it has the following limitations:

<ul>
<li>The function returns an <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation token</a>, not a primary token. You cannot use this token directly in the 
<a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a> function. However, you can call the 
<a href="https://msdn.microsoft.com/96b13826-0ac7-4d70-9c21-eeb343f6b823">DuplicateTokenEx</a> function to convert the token to a primary token, and then use it in <b>CreateProcessAsUser</b>.</li>
<li>If you convert the token to a primary token and use it in <a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a> to start a process, the new process cannot access other network resources, such as remote servers or printers, through the redirector. An exception is that if the network resource is not access controlled, then the new process will be able to access it.</li>
</ul>


The SE_TCB_NAME privilege is not required for this function unless you are logging onto a Passport account.

The account specified by <i>lpszUsername</i> must have the necessary account rights. For example, to log on a user with the LOGON32_LOGON_INTERACTIVE flag, the user (or a group to which the user belongs) must have the SE_INTERACTIVE_LOGON_NAME account right. For a list of the account rights that affect the various logon operations, see 
<a href="https://msdn.microsoft.com/42fb22bb-8135-4a8f-bce6-e767d6c5aaea">Account Object Access Rights</a>.

A user is considered logged on if at least one token exists. If you call 
<a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a> and then close the token, the user is still logged on until the process (and all child processes) have ended.

If the <b>LogonUserEx</b> call is successful, the system notifies network providers that the logon occurred by calling the provider's <a href="https://msdn.microsoft.com/9b0e5646-ac57-4eae-bad7-a16c07b51f4b">NPLogonNotify</a> entry-point function.




## -see-also




<a href="https://msdn.microsoft.com/8301ed4f-9458-410b-af19-4f055656005a">Client/Server Access Control</a>



<a href="https://msdn.microsoft.com/c236f335-b5de-4e8b-851d-45e008791271">Client/Server Access Control Functions</a>



<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a>



<a href="https://msdn.microsoft.com/96b13826-0ac7-4d70-9c21-eeb343f6b823">DuplicateTokenEx</a>



<a href="https://msdn.microsoft.com/cf5c31ae-6749-45c2-888f-697060cc8c75">ImpersonateLoggedOnUser</a>



<a href="https://msdn.microsoft.com/7514ec77-34b1-490d-ba21-3b6944942aa7">QUOTA_LIMITS</a>
 

 

