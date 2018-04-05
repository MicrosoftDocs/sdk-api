---
UID: NE:ntsecapi._MSV1_0_PROTOCOL_MESSAGE_TYPE
title: "_MSV1_0_PROTOCOL_MESSAGE_TYPE"
author: windows-driver-content
description: Lists the types of messages that can be sent to the MSV1_0 Authentication Package by calling the LsaCallAuthenticationPackage function.
old-location: security\msv1_0_protocol_message_type.htm
old-project: SecAuthN
ms.assetid: 9498558c-8daf-4dfb-aa1c-0598154ca8c4
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: "*PMSV1_0_PROTOCOL_MESSAGE_TYPE, MSV1_0_PROTOCOL_MESSAGE_TYPE, MSV1_0_PROTOCOL_MESSAGE_TYPE enumeration [Security], MsV1_0CacheLogon, MsV1_0CacheLookup, MsV1_0CacheLookupEx, MsV1_0ChangeCachedPassword, MsV1_0ChangePassword, MsV1_0ClearCachedCredentials, MsV1_0ConfigLocalAliases, MsV1_0DeriveCredential, MsV1_0EnumerateUsers, MsV1_0GenericPassthrough, MsV1_0GetCredentialKey, MsV1_0GetUserInfo, MsV1_0Lm20ChallengeRequest, MsV1_0Lm20GetChallengeResponse, MsV1_0LookupToken, MsV1_0ReLogonUsers, MsV1_0SetProcessOption, MsV1_0SetThreadOption, MsV1_0SubAuth, MsV1_0ValidateAuth, PMSV1_0_PROTOCOL_MESSAGE_TYPE, PMSV1_0_PROTOCOL_MESSAGE_TYPE enumeration pointer [Security], _MSV1_0_PROTOCOL_MESSAGE_TYPE, _lsa_msv1_0_protocol_message_type, ntsecapi/MSV1_0_PROTOCOL_MESSAGE_TYPE, ntsecapi/MsV1_0CacheLogon, ntsecapi/MsV1_0CacheLookup, ntsecapi/MsV1_0CacheLookupEx, ntsecapi/MsV1_0ChangeCachedPassword, ntsecapi/MsV1_0ChangePassword, ntsecapi/MsV1_0ClearCachedCredentials, ntsecapi/MsV1_0ConfigLocalAliases, ntsecapi/MsV1_0DeriveCredential, ntsecapi/MsV1_0EnumerateUsers, ntsecapi/MsV1_0GenericPassthrough, ntsecapi/MsV1_0GetCredentialKey, ntsecapi/MsV1_0GetUserInfo, ntsecapi/MsV1_0Lm20ChallengeRequest, ntsecapi/MsV1_0Lm20GetChallengeResponse, ntsecapi/MsV1_0LookupToken, ntsecapi/MsV1_0ReLogonUsers, ntsecapi/MsV1_0SetProcessOption, ntsecapi/MsV1_0SetThreadOption, ntsecapi/MsV1_0SubAuth, ntsecapi/MsV1_0ValidateAuth, ntsecapi/PMSV1_0_PROTOCOL_MESSAGE_TYPE, security.msv1_0_protocol_message_type"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: MSV1_0_PROTOCOL_MESSAGE_TYPE, *PMSV1_0_PROTOCOL_MESSAGE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntsecapi.h
api_name:
-	MSV1_0_PROTOCOL_MESSAGE_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _MSV1_0_PROTOCOL_MESSAGE_TYPE enumeration


## -description


The <b>MSV1_0_PROTOCOL_MESSAGE_TYPE</b> enumeration lists the types of messages that can be sent to the 
<a href="https://msdn.microsoft.com/8b85588d-0a79-43af-b526-7a5fc8248f99">MSV1_0 Authentication Package</a> by calling the 
<a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a> function.

 Each message corresponds to a dispatch routine and causes the MSV1_0 authentication package to perform a different task.


## -enum-fields




### -field MsV1_0Lm20ChallengeRequest

This dispatch routine serves as the first half of an NTLM version 2.0 protocol logon. The challenge returned by this call may be delivered to the initiating NTLM 2.0 node. When that node responds with a challenge response, a <b>MsV1_0Lm20Logon</b> message to the 
<a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a> function is used to complete the logon. For more information, see 
<a href="https://msdn.microsoft.com/03bf43f0-44f4-40c6-8d5d-381f36ebdd0e">MSV1_0_LOGON_SUBMIT_TYPE</a>.


### -field MsV1_0Lm20GetChallengeResponse

This dispatch routine is used by the NTLM redirector to determine the challenge response to pass to a server when trying to establish a connection to the server. 




This routine is passed a challenge from the server. It then encrypts the challenge with either the specified password or with the password implied by the specified <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon identifier</a>. Two challenge responses are returned. One is based on the <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> password as given to the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">authentication package</a>. The other is based on that password converted to a multiple-byte character set (for example, ASCII) and uppercase. The redirector should use either (or both) formats of challenge responses as it needs them. The redirector should use the returned challenge responses exactly as returned. No zero byte should be added. A challenge response is binary data and might contain zero bytes within the string.

This routine may indicate that a <b>NULL</b> session is to be used. If the redirector specifies all the RETURN_PRIMARY_DOMAINNAME, RETURN_PRIMARY_USERNAME, and USE_PRIMARY_PASSWORD flags, and the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon ID</a> does not correspond to any interactive <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon session</a>, this function returns an empty string for the user name and both challenge responses.


### -field MsV1_0EnumerateUsers

This value is obsolete.


### -field MsV1_0GetUserInfo

This value is obsolete.


### -field MsV1_0ReLogonUsers

This value is not supported.


### -field MsV1_0ChangePassword

This dispatch routine changes the password of an account.


### -field MsV1_0ChangeCachedPassword

 This dispatch routine changes a password in the logon cache. This is used when the password is changed on the domain controller using some other mechanism and the locally cached version needs to be updated to match the new value. For example, RAS handles changing the passwords on the domain but then needs to update the cached copy so the user can still access servers.


### -field MsV1_0GenericPassthrough

 This dispatch routine passes any of the other dispatch routines to the domain controller. The authentication package on the domain controller may choose to reject certain dispatch requests.


### -field MsV1_0CacheLogon

 This dispatch routine caches logon information in the logon cache.


### -field MsV1_0SubAuth

 This dispatch routine is called to submit a buffer to a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subauthentication package</a>. If the subauthentication is local, use this dispatch routine. If the subauthentication needs to be processed on the domain controller, use the <b>MsV1_0GenericPassthrough</b> dispatch routine with 
<a href="https://msdn.microsoft.com/5a408c0a-56d4-48f6-8289-6f203ef998df">MSV1_0_SUBAUTH_REQUEST</a> and 
<a href="https://msdn.microsoft.com/62808fba-6e10-4f3b-a705-6958fc4fe480">MSV1_0_SUBAUTH_RESPONSE</a> buffers.


### -field MsV1_0DeriveCredential

This dispatch routine gets the <b>HMAC_SHA1</b> hash of the  one-way function password of the current logon session.  



### -field MsV1_0CacheLookup

Reserved. Do not use.


### -field MsV1_0SetProcessOption

This dispatch routine sets the password policy. The <b>SeTcbPrivilege</b> is required. 



### -field MsV1_0ConfigLocalAliases

This dispatch routine adds, deletes, or enumerates registered local aliases. The caller must be a service to use this message type.

<b>Windows Server 2003 and Windows XP:  </b>Not supported.


### -field MsV1_0ClearCachedCredentials

This dispatch routine clears the credentials in the local NTLM logon cache. The <b>SeTcbPrivilege</b> is required.

<b>Windows Server 2003 and Windows XP:  </b>Not supported.


### -field MsV1_0LookupToken

This dispatch routine looks up the authentication  token. The <b>SeTcbPrivilege</b> is required.

<b>Windows Server 2003 with SP2, Windows Vista, Windows Server 2003 and Windows XP:  </b>Not supported.


### -field MsV1_0ValidateAuth

This dispatch routine  validates the logon authentication. The <b>SeTcbPrivilege</b> is required.

<b>Windows Server 2008, Windows Vista with SP1, Windows Server 2003 with SP2, Windows Vista, Windows Server 2003 and Windows XP:  </b>Not supported.


### -field MsV1_0CacheLookupEx

This dispatch routine  looks up the local logon in the cache. The <b>SeTcbPrivilege</b> is required.

<b>Windows Server 2008, Windows Vista with SP1, Windows Server 2003 with SP2, Windows Vista, Windows Server 2003 and Windows XP:  </b>Not supported.


### -field MsV1_0GetCredentialKey

This dispatch routine  gets the credential key of the authentication packet. The <b>SeTcbPrivilege</b> is required.

<b>Windows Server 2008, Windows Vista with SP1, Windows Server 2003 with SP2, Windows Vista, Windows Server 2003 and Windows XP:  </b>Not supported.


### -field MsV1_0SetThreadOption

This dispatch routine sets the features and permissions on  the calling thread. Thread options take precedence over process options and should be used in place of NTLM process options. The <b>SeTcbPrivilege</b> is required.

<b>Windows Server 2008, Windows Vista with SP1, Windows Server 2003 with SP2, Windows Vista, Windows Server 2003 and Windows XP:  </b>Not supported.


### -field MsV1_0DecryptDpapiMasterKey


### -field MsV1_0GetStrongCredentialKey


### -field MsV1_0TransferCred


### -field MsV1_0ProvisionTbal


### -field MsV1_0DeleteTbalSecrets



