---
UID: NS:credentialprovider._CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION
title: CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION (credentialprovider.h)
description: Contains details about a credential.
helpviewer_keywords: ["CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION","CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION structure [Windows Shell]","_shell_CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION","credentialprovider/CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION","shell.CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION"]
old-location: shell\CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION.htm
tech.root: shell
ms.assetid: 55ff9be3-490d-4f82-92a0-3551ccbcaade
ms.date: 12/05/2018
ms.keywords: CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION, CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION structure [Windows Shell], _shell_CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION, credentialprovider/CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION, shell.CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION
 - credentialprovider/_CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION
 - CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION
 - credentialprovider/CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Credentialprovider.h
api_name:
 - CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION
---

# CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION structure


## -description

Contains details about a credential.

## -struct-fields

### -field ulAuthenticationPackage

Type: <b>ULONG</b>

The unique identifier of the authentication package. This parameter is required when calling <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a>.  In a Credential UI scenario, this value is set before a serialization is sent through <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovider-setserialization">SetSerialization</a>. This is the same as the authentication package value returned by <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupauthenticationpackage">LsaLookupAuthenticationPackage</a>. Content providers can use this parameter to determine if they are able to return credentials for this authentication package. Developers who write their own authentication package may supply their own value.

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

Once the user has entered credential information into a credential tile, it needs to be put into a buffer. Packaging up this information is called serialization and is necessary regardless of whether the scenario uses a Logon UI or a Credential UI. The <b>CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</b> defines the structure for serialization. After serialization, where the buffer is sent depends on whether it is a Logon UI or Credential UI scenario. With a Logon UI, the buffer is passed to <a href="/windows/desktop/SecAuthN/winlogon">Winlogon</a>. In the Credential UI scenario, this buffer is returned to the calling application which then uses it to authenticate the user.

<div class="alert"><b>Important</b>  <p class="note">Even if you are implementing a <a href="/windows/win32/api/credentialprovider/ne-credentialprovider-credential_provider_usage_scenario">CREDENTIAL_PROVIDER_USAGE_SCENARIO</a> of <b>CPUS_LOGON</b>, you do not directly call <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a>. That call is handled by the system. You merely need to pass your credentials to <a href="/windows/desktop/SecAuthN/winlogon">Winlogon</a>.

</div>
<div> </div>
Credential providers may also enumerate a credential tile if an input credential is received from <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovider-setserialization">SetSerialization</a>. One example where this is useful is if a user provides an invalid user-password combination. The Credential UI will pass the credentials back to the credential provider since they are invalid. The credential provider can opt to display a tile to the user that already has the user name filled in.

Input credentials can take many different forms. It is important that credential providers are robust when receiving serialized credentials. This could include incomplete or partial credentials. In many cases, an incomplete input credential is a hint about what type of credential the caller wants. One case where this process is used is with callers who only wish to gather smart card credentials from the user. During the <b>CPUS_LOGON</b> usage scenario, the system uses <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovider-setserialization">SetSerialization</a> to fill in some of the information from a remote machine. Logon UI will call <b>SetSerialization</b> zero or one times each enumeration cycle.