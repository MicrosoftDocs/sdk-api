---
UID: NF:ntsecapi.LsaLogonUser
title: LsaLogonUser function
author: windows-driver-content
description: Authenticates a security principal's logon data by using stored credentials information.
old-location: security\lsalogonuser.htm
old-project: SecAuthN
ms.assetid: 75968d53-5af2-4d77-9486-26403b73c954
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: KERB_CERTIFICATE_LOGON, KERB_CERTIFICATE_S4U_LOGON, KERB_CERTIFICATE_UNLOCK_LOGON, KERB_INTERACTIVE_LOGON, KERB_S4U_LOGON, KERB_SMARTCARD_LOGON, KERB_SMARTCARD_UNLOCK_LOGON, KERB_TICKET_LOGON, KERB_TICKET_PROFILE, KERB_TICKET_UNLOCK_LOGON, LsaLogonUser, LsaLogonUser function [Security], MSV1_0_INTERACTIVE_LOGON, MSV1_0_INTERACTIVE_PROFILE, MSV1_0_LM20_LOGON, MSV1_0_LM20_LOGON_PROFILE, MSV1_0_SUBAUTH_LOGON, STATUS_ACCOUNT_DISABLED, STATUS_INVALID_LOGON_HOURS, STATUS_INVALID_WORKSTATION, STATUS_PASSWORD_EXPIRED, _lsa_lsalogonuser, ntsecapi/LsaLogonUser, security.lsalogonuser
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntsecapi.h
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
req.typenames: TRUSTED_INFORMATION_CLASS, *PTRUSTED_INFORMATION_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Secur32.dll
api_name:
-	LsaLogonUser
product: Windows
targetos: Windows
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# LsaLogonUser function


## -description


The <b>LsaLogonUser</b> function authenticates a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security principal's</a> logon data by using stored credentials information.

If the authentication is successful, this function creates a new logon session and returns a user token.

When a new ticket granting ticket (TGT) is obtained by using new certificate credentials, then all of the system's TGTs and service tickets are purged. Any user service tickets that are of a compound identity are also purged.


## -parameters




### -param LsaHandle [in]

A handle obtained from a previous call to 
<a href="https://msdn.microsoft.com/1bef2949-b4c8-400e-8a2d-60aa88a4e238">LsaRegisterLogonProcess</a>.

The caller is required to have <b>SeTcbPrivilege</b> only if one or more of the following is true:

<ul>
<li>A Subauthentication package is used.</li>
<li>
<a href="https://msdn.microsoft.com/ab94c36b-7aba-452d-abc0-220c91ffacca">KERB_S4U_LOGON</a> is used, and the caller requests an impersonation token.</li>
<li>The <i>LocalGroups</i> parameter is not <b>NULL</b>.</li>
</ul>
 If <b>SeTcbPrivilege</b> is not required, call <a href="https://msdn.microsoft.com/b54917c8-51cd-4891-9613-f37a4a46448b">LsaConnectUntrusted</a> to obtain the handle.


### -param OriginName [in]

A string that identifies the origin of the logon attempt. For more information, see Remarks.


### -param LogonType [in]

A 
value of the <a href="https://msdn.microsoft.com/d775d782-9403-47b2-bb43-8f677db49eb9">SECURITY_LOGON_TYPE</a> enumeration that specifies the type of logon requested. If <i>LogonType</i> is Interactive or Batch, a primary token is generated to represent the new user. If <i>LogonType</i> is Network, an impersonation token is generated.


### -param AuthenticationPackage [in]

An identifier of the authentication package to use for the authentication. You can obtain this value by calling 
<a href="https://msdn.microsoft.com/c6504aea-fdba-44ac-b2dc-070707bb1183">LsaLookupAuthenticationPackage</a>.


### -param AuthenticationInformation [in]

A pointer to an input buffer that contains authentication information, such as user name and password. The format and content of this buffer are determined by the authentication package.

This parameter can be one of the following input buffer structures for the MSV1_0 and Kerberos authentication packages.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSV1_0_INTERACTIVE_LOGON"></a><a id="msv1_0_interactive_logon"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/f9b9a966-54b9-4f89-98cc-d92e3f74571d">MSV1_0_INTERACTIVE_LOGON</a></b></dt>
<dt>MSV1_0</dt>
</dl>
</td>
<td width="60%">
Authenticating an interactive user logon.

The <b>LogonDomainName</b>,  <b>UserName</b>, and <b>Password </b> members of the <a href="https://msdn.microsoft.com/ab94c36b-7aba-452d-abc0-220c91ffacca">MSV1_0_INTERACTIVE_LOGON</a> structure must point to buffers in memory that are contiguous to the structure itself. The value of the <i>AuthenticationInformationLength</i> parameter must take into account the length of these buffers.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_INTERACTIVE_LOGON"></a><a id="kerb_interactive_logon"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/96aec0cc-b3e1-4b4b-aa0e-ecf05b9fabbe">KERB_INTERACTIVE_LOGON</a></b></dt>
<dt>Kerberos</dt>
</dl>
</td>
<td width="60%">
Authenticating an interactive user logon.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_LOGON"></a><a id="kerb_ticket_logon"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/2c082c79-ce7f-45a1-8552-3b4e9034b7e3">KERB_TICKET_LOGON</a></b></dt>
<dt>Kerberos</dt>
</dl>
</td>
<td width="60%">
Authenticating a user on initial network logon or disconnect.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_UNLOCK_LOGON"></a><a id="kerb_ticket_unlock_logon"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/24daa3d1-1116-4b0b-a19b-a23075a69197">KERB_TICKET_UNLOCK_LOGON</a></b></dt>
<dt>Kerberos</dt>
</dl>
</td>
<td width="60%">
Authenticating a user on ticket refresh, a variation of the normal workstation unlock logon.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_CERTIFICATE_LOGON"></a><a id="kerb_certificate_logon"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/e6aa0042-edb5-4e9b-b545-5159d3bfb8fc">KERB_CERTIFICATE_LOGON</a></b></dt>
<dt>Kerberos</dt>
</dl>
</td>
<td width="60%">
Authenticating a user using an interactive smart card logon.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_CERTIFICATE_S4U_LOGON"></a><a id="kerb_certificate_s4u_logon"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/C7BF8A80-493E-4BDB-ACE3-F9492C71BCA9">KERB_CERTIFICATE_S4U_LOGON</a></b></dt>
<dt>Kerberos</dt>
</dl>
</td>
<td width="60%">
Authenticating a user using a service for user (S4U) logon.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_CERTIFICATE_UNLOCK_LOGON"></a><a id="kerb_certificate_unlock_logon"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/04e058b0-9a05-4ed7-9d4a-1c8c003d8077">KERB_CERTIFICATE_UNLOCK_LOGON</a></b></dt>
<dt>Kerberos</dt>
</dl>
</td>
<td width="60%">
Authenticating a user to unlock a workstation that has been locked during an interactive smart card logon session.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_SMARTCARD_LOGON"></a><a id="kerb_smartcard_logon"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/1a154034-6a2d-46be-9fb6-7c7d425d12f6">KERB_SMARTCARD_LOGON</a></b></dt>
<dt>Kerberos</dt>
</dl>
</td>
<td width="60%">
Authenticating a user smart card logon using LOGON32_PROVIDER_WINNT50 or LOGON32_PROVIDER_DEFAULT.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_SMARTCARD_UNLOCK_LOGON"></a><a id="kerb_smartcard_unlock_logon"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/5fcd61f6-d93d-4047-b472-8b44f9681907">KERB_SMARTCARD_UNLOCK_LOGON</a></b></dt>
<dt>Kerberos</dt>
</dl>
</td>
<td width="60%">
Authenticating a user to unlock a workstation that has been locked during a smart card logon session.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_S4U_LOGON"></a><a id="kerb_s4u_logon"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/ab94c36b-7aba-452d-abc0-220c91ffacca">KERB_S4U_LOGON</a></b></dt>
<dt>Kerberos</dt>
</dl>
</td>
<td width="60%">
Authenticating a user using S4U client requests. For <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">constrained delegation</a>, a call to LsaLogonUser is not necessary if the client logged on using an LSA-mode authentication package. On Windows operating systems, these include <a href="https://msdn.microsoft.com/e7870e72-1386-4818-bf6f-73430ae942a8">Kerberos</a>, <a href="https://msdn.microsoft.com/35a38858-d36f-45c9-95f4-2541a182f5ac">NTLM</a>, <a href="https://msdn.microsoft.com/159074a1-6425-409a-8470-02cd485b75e9">Secure Channel</a>, and <a href="https://msdn.microsoft.com/0b7d67c9-00ac-4b04-bf8e-97aaf1020108">Digest</a>. For this call to succeed, the following must be true:

<ul>
<li>The caller must be a domain account (this includes LOCAL_SYSTEM if the computer is a domain member).</li>
<li>If using a service account, the account must have <b>SeTcbPrivilege</b> set on the local computer to get an impersonation token. Otherwise, the identity token is used.</li>
<li>The caller must be a member of the <b>Pre-Windows 2000 Compatible Access</b> or have read access to the group memberships of the client. Membership in the Windows Authorization Access group guarantees read access to group membership of the client. For information about how to configure the Windows Authorization Access group, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=83978">Microsoft Knowledge Base</a>.</li>
</ul>
The <b>ClientUpn</b> and <b>ClientRealm</b> members of the <a href="https://msdn.microsoft.com/ab94c36b-7aba-452d-abc0-220c91ffacca">KERB_S4U_LOGON</a> structure must point to buffers in memory that are contiguous to the structure itself. The value of the <i>AuthenticationInformationLength</i> parameter must take into account the length of these buffers.

</td>
</tr>
<tr>
<td width="40%"><a id="MSV1_0_LM20_LOGON"></a><a id="msv1_0_lm20_logon"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/0736ab5b-a475-4593-a15e-970b5d4c64d0">MSV1_0_LM20_LOGON</a></b></dt>
<dt>MSV1_0</dt>
</dl>
</td>
<td width="60%">
Processing the second half of an NTLM 2.0 protocol logon. The first half of this type of logon is performed by calling 
<a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a> with the <b>MsV1_0Lm20ChallengeRequest</b> message. For more information, see the description of <b>MsV1_0Lm20ChallengeRequest</b> in 
<a href="https://msdn.microsoft.com/9498558c-8daf-4dfb-aa1c-0598154ca8c4">MSV1_0_PROTOCOL_MESSAGE_TYPE</a>.

This type of logon can use a subauthentication package.

</td>
</tr>
<tr>
<td width="40%"><a id="MSV1_0_SUBAUTH_LOGON"></a><a id="msv1_0_subauth_logon"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/e53cb14a-097c-4ee4-ab7a-baa4b6699cc7">MSV1_0_SUBAUTH_LOGON</a></b></dt>
<dt>MSV1_0</dt>
</dl>
</td>
<td width="60%">
Authenticating a user with subauthentication.

</td>
</tr>
</table>
 

For more information about the buffer used by other authentication packages, see the documentation for those authentication packages.


### -param AuthenticationInformationLength [in]

The length, in bytes, of the <i>AuthenticationInformation</i> buffer.


### -param LocalGroups [in, optional]

A list of additional group identifiers to add to the token of the authenticated user. These group identifiers will be added, along with the default group WORLD and the logon type group (Interactive, Batch, or Network), which are automatically included in every user token.


### -param SourceContext [in]

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff556848">TOKEN_SOURCE</a> structure that identifies the source module—for example, the session manager—and the context that may be useful to that module. This information is included in the user token and can be retrieved by calling 
<a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a>.


### -param ProfileBuffer [out]

A pointer to a void pointer that receives the address of an output buffer that contains authentication information, such as the logon shell and home directory.

This parameter can be one of the following output buffer structures for the MSV1_0 and Kerberos authentication packages.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSV1_0_INTERACTIVE_PROFILE"></a><a id="msv1_0_interactive_profile"></a><dl>
<dt><b>MSV1_0_INTERACTIVE_PROFILE</b></dt>
<dt>MSV1_0</dt>
</dl>
</td>
<td width="60%">
An interactive user's logon profile.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_PROFILE"></a><a id="kerb_ticket_profile"></a><dl>
<dt><b>KERB_TICKET_PROFILE</b></dt>
<dt>Kerberos</dt>
</dl>
</td>
<td width="60%">
Logon, disconnect, and ticket refresh authentication output.

</td>
</tr>
<tr>
<td width="40%"><a id="MSV1_0_LM20_LOGON"></a><a id="msv1_0_lm20_logon"></a><dl>
<dt><b>MSV1_0_LM20_LOGON</b></dt>
<dt>MSV1_0</dt>
</dl>
</td>
<td width="60%">
Output when processing the second half of a NTLM 2.0 protocol logon.

</td>
</tr>
<tr>
<td width="40%"><a id="MSV1_0_LM20_LOGON_PROFILE"></a><a id="msv1_0_lm20_logon_profile"></a><dl>
<dt><b>MSV1_0_LM20_LOGON_PROFILE</b></dt>
<dt>MSV1_0</dt>
</dl>
</td>
<td width="60%">
Output when using authentication with subauthentication.

</td>
</tr>
</table>
 

For more information about the buffer used by other authentication packages, see the documentation for that authentication package.

When this buffer is no longer needed, the calling application must free this buffer by calling 
the <a href="https://msdn.microsoft.com/e814ed68-07e7-4936-ba96-5411086f43f6">LsaFreeReturnBuffer</a> function.


### -param ProfileBufferLength [out]

A pointer to a <b>ULONG</b> that receives the length, in bytes, of the returned profile buffer.


### -param LogonId [out]

A pointer to a buffer that receives an 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a> that uniquely identifies the logon session. This <b>LUID</b> is assigned by the domain controller that authenticated the logon information.


### -param Token [out]

A pointer to a handle that receives the new user token created for this session. When you have finished using the token, release it by calling the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function.


### -param Quotas [out]

When a primary token is returned, this parameter receives a 
<a href="https://msdn.microsoft.com/7514ec77-34b1-490d-ba21-3b6944942aa7">QUOTA_LIMITS</a> structure that contains the process quota limits assigned to the newly logged on user's initial process.


### -param SubStatus [out]

If the logon failed due to account restrictions, this parameter receives information about why the logon failed. This value is set only if the account information of the user is valid and the logon is rejected.

This parameter can be one of the following <i>SubStatus</i> values for the MSV1_0 authentication package.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STATUS_INVALID_LOGON_HOURS"></a><a id="status_invalid_logon_hours"></a><dl>
<dt><b>STATUS_INVALID_LOGON_HOURS</b></dt>
</dl>
</td>
<td width="60%">
The user account has time restrictions and cannot be used to log on at this time.

</td>
</tr>
<tr>
<td width="40%"><a id="STATUS_INVALID_WORKSTATION"></a><a id="status_invalid_workstation"></a><dl>
<dt><b>STATUS_INVALID_WORKSTATION</b></dt>
</dl>
</td>
<td width="60%">
The user account has workstation restrictions and cannot be used to log on from the current workstation.

</td>
</tr>
<tr>
<td width="40%"><a id="STATUS_PASSWORD_EXPIRED"></a><a id="status_password_expired"></a><dl>
<dt><b>STATUS_PASSWORD_EXPIRED</b></dt>
</dl>
</td>
<td width="60%">
The user-account password has expired.

</td>
</tr>
<tr>
<td width="40%"><a id="STATUS_ACCOUNT_DISABLED"></a><a id="status_account_disabled"></a><dl>
<dt><b>STATUS_ACCOUNT_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
The user account is currently disabled and cannot be used to log on.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the function returns  STATUS_SUCCESS.

If the function fails, it returns  an <b>NTSTATUS</b> code, which can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
The caller's memory quota is insufficient to allocate the output buffer returned by the authentication package.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_ACCOUNT_RESTRICTION</b></dt>
</dl>
</td>
<td width="60%">
The user account and password are legitimate, but the user account has a restriction that prevents logon at this time. For more information, see the value stored in the <i>SubStatus</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_BAD_VALIDATION_CLASS</b></dt>
</dl>
</td>
<td width="60%">
The authentication information provided is not recognized by the authentication package.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_LOGON_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The logon attempt failed. The reason for the failure is not specified, but typical reasons include misspelled user names and misspelled passwords.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_LOGON_SERVERS</b></dt>
</dl>
</td>
<td width="60%">
No domain controllers are available to service the authentication request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_SUCH_PACKAGE</b></dt>
</dl>
</td>
<td width="60%">
The specified authentication package is not recognized by the LSA.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_PKINIT_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The Kerberos client received a KDC certificate that is not valid. For device logon, strict KDC validation is required, so the KDC must have certificates that use the "Kerberos Authentication" template or equivalent. Also, the KDC certificate could be expired, revoked, or the client is under active attack of sending requests to the wrong server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_PKINIT_CLIENT_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The Kerberos client is using a system certificate that is not valid. For device logon, there must be a DNS name. Also, the system certificate could be expired or the wrong one could be selected.

</td>
</tr>
</table>
 

For more information, see 
<a href="https://msdn.microsoft.com/ee55364e-8ffe-4a78-a49a-250756561770">LSA Policy Function Return Values</a>.

The 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function converts an <b>NTSTATUS</b> code to a Windows error code.




## -remarks



The <i>OriginName</i> parameter should specify meaningful information. For example, it might contain "TTY1" to indicate terminal one or "NTLM - remote node JAZZ" to indicate a network logon that uses NTLM through a remote node called "JAZZ".

You must call <b>LsaLogonUser</b> separately to update PKINIT device credentials for LOCAL_SYSTEM and NETWORK_SERVICE. When there is no PKINIT device credential, a successful call does no operation. When there is a PKINIT device credential, a successful call cleans up the PKINIT device credential so that only the password credential remains.




## -see-also




<a href="https://msdn.microsoft.com/3d813e46-f06e-4147-874c-30b5fc6f50d9">Allowing Anonymous Access</a>



<a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a>



<a href="https://msdn.microsoft.com/e814ed68-07e7-4936-ba96-5411086f43f6">LsaFreeReturnBuffer</a>



<a href="https://msdn.microsoft.com/c6504aea-fdba-44ac-b2dc-070707bb1183">LsaLookupAuthenticationPackage</a>
 

 

