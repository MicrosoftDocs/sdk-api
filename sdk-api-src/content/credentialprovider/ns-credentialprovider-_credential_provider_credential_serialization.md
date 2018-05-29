---
UID: NS:credentialprovider._CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION
title: "_CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION"
author: windows-sdk-content
description: Contains details about a credential.
old-location: shell\CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION.htm
old-project: shell
ms.assetid: 55ff9be3-490d-4f82-92a0-3551ccbcaade
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION, CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION structure [Windows Shell], _CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION, _shell_CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION, credentialprovider/CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION, shell.CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: credentialprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Credentialprovider.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Credentialprovider.h
api_name:
-	CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION structure


## -description


Contains details about a credential.


## -struct-fields




### -field ulAuthenticationPackage

Type: <b>ULONG</b>

The unique identifier of the authentication package. This parameter is required when calling <a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a>.  In a Credential UI scenario, this value is set before a serialization is sent through <a href="https://msdn.microsoft.com/eeeaa3b8-ad0f-4d31-bdd1-646b0e33b7cd">SetSerialization</a>. This is the same as the authentication package value returned by <a href="https://msdn.microsoft.com/c6504aea-fdba-44ac-b2dc-070707bb1183">LsaLookupAuthenticationPackage</a>. Content providers can use this parameter to determine if they are able to return credentials for this authentication package. Developers who write their own authentication package may supply their own value.


### -field clsidCredentialProvider

Type: <b>GUID</b>

The CLSID of the credential provider. Credential providers assign their own CLSID to this member during serialization. Credential UI ignores this member.


### -field cbSerialization

Type: <b>ULONG</b>

The size, in bytes, of the credential pointed to by <b>rgbSerialization</b>.


### -field rgbSerialization

Type: <b>byte*</b>

An array of bytes containing serialized credential information. The exact format of this data depends on the authentication package targeted by a credential provider.


## -remarks



Once the user has entered credential information into a credential tile, it needs to be put into a buffer. Packaging up this information is called serialization and is necessary regardless of whether the scenario uses a Logon UI or a Credential UI. The <b>CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</b> defines the structure for serialization. After serialization, where the buffer is sent depends on whether it is a Logon UI or Credential UI scenario. With a Logon UI, the buffer is passed to <a href="https://msdn.microsoft.com/library/windows/hardware/dn927313">Winlogon</a>. In the Credential UI scenario, this buffer is returned to the calling application which then uses it to authenticate the user.

<div class="alert"><b>Important</b>  <p class="note">Even if you are implementing a <a href="https://msdn.microsoft.com/86025d1d-b13d-4f61-824a-fd471e449567">CREDENTIAL_PROVIDER_USAGE_SCENARIO</a> of <b>CPUS_LOGON</b>, you do not directly call <a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a>. That call is handled by the system. You merely need to pass your credentials to <a href="https://msdn.microsoft.com/library/windows/hardware/dn927313">Winlogon</a>.

</div>
<div> </div>
Credential providers may also enumerate a credential tile if an input credential is received from <a href="https://msdn.microsoft.com/eeeaa3b8-ad0f-4d31-bdd1-646b0e33b7cd">SetSerialization</a>. One example where this is useful is if a user provides an invalid user-password combination. The Credential UI will pass the credentials back to the credential provider since they are invalid. The credential provider can opt to display a tile to the user that already has the user name filled in.

Input credentials can take many different forms. It is important that credential providers are robust when receiving serialized credentials. This could include incomplete or partial credentials. In many cases, an incomplete input credential is a hint about what type of credential the caller wants. One case where this process is used is with callers who only wish to gather smart card credentials from the user. During the <b>CPUS_LOGON</b> usage scenario, the system uses <a href="https://msdn.microsoft.com/eeeaa3b8-ad0f-4d31-bdd1-646b0e33b7cd">SetSerialization</a> to fill in some of the information from a remote machine. Logon UI will call <b>SetSerialization</b> zero or one times each enumeration cycle.  



