---
UID: NF:credentialprovider.ICredentialProvider.GetCredentialCount
title: ICredentialProvider::GetCredentialCount (credentialprovider.h)
description: Gets the number of available credentials under this credential provider.
helpviewer_keywords: ["GetCredentialCount","GetCredentialCount method [Windows Shell]","GetCredentialCount method [Windows Shell]","ICredentialProvider interface","ICredentialProvider interface [Windows Shell]","GetCredentialCount method","ICredentialProvider.GetCredentialCount","ICredentialProvider::GetCredentialCount","credentialprovider/ICredentialProvider::GetCredentialCount","shell.ICredentialProvider_GetCredentialCount","shell_ICredentialProvider_GetCredentialCount"]
old-location: shell\ICredentialProvider_GetCredentialCount.htm
tech.root: shell
ms.assetid: 7d940d46-d4c2-4ab5-8559-416d78d3579e
ms.date: 12/05/2018
ms.keywords: GetCredentialCount, GetCredentialCount method [Windows Shell], GetCredentialCount method [Windows Shell],ICredentialProvider interface, ICredentialProvider interface [Windows Shell],GetCredentialCount method, ICredentialProvider.GetCredentialCount, ICredentialProvider::GetCredentialCount, credentialprovider/ICredentialProvider::GetCredentialCount, shell.ICredentialProvider_GetCredentialCount, shell_ICredentialProvider_GetCredentialCount
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICredentialProvider::GetCredentialCount
 - credentialprovider/ICredentialProvider::GetCredentialCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Credentialprovider.h
api_name:
 - ICredentialProvider.GetCredentialCount
---

# ICredentialProvider::GetCredentialCount


## -description

Gets the number of available credentials under this credential provider.

## -parameters

### -param pdwCount [out]

Type: <b>DWORD*</b>

A pointer to a <b>DWORD</b> value that receives the count of credentials.

### -param pdwDefault [out]

Type: <b>DWORD*</b>

A pointer to a <b>DWORD</b> value that receives the index of the credential to be used as the default. If no default value has been set, this value should be set to <b>CREDENTIAL_PROVIDER_NO_DEFAULT</b>.

### -param pbAutoLogonWithDefault [out]

Type: <b>BOOL*</b>

A pointer to a <b>BOOL</b> value indicating if the default credential identified by <i>pdwDefault</i> should be used for an auto logon attempt. An auto logon attempt means the Logon UI or Credential UI will immediately call <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-getserialization">GetSerialization</a> on the provider's default tile.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is required.

When a Logon UI or Credential UI is ready for user interaction, a default credential is selected by default. Since each credential provider supplies a default credential, the following rules determine if <i>pdwDefault</i> will receive focus or if the credential will be automatically logged in.

<ul>
<li>If a default credential has already been specified, that credential is not intended to be used for auto logon, and the <i>pdwDefault</i> is used for auto logon, then <i>pdwDefault</i> will be used as the default.</li>
<li>If <i>pdwDefault</i> is from the last logged on provider and there isn't already a default with auto logon, then <i>pdwDefault</i> will be used as the default.</li>
<li>If no default has been specified, then <i>pdwDefault</i> will be used as the default.</li>
</ul>
If the number of valid credentials change, the credential provider should call <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialproviderevents-credentialschanged">CredentialsChanged</a> on the  <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialproviderevents">ICredentialProviderEvents</a> instance provided in <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovider-advise">Advise</a>.

<h3><a id="Credential_Provider_Best_Practices"></a><a id="credential_provider_best_practices"></a><a id="CREDENTIAL_PROVIDER_BEST_PRACTICES"></a>Credential Provider Best Practices</h3>
Credential providers handle extremely sensitive user secrets in order to complete logon and unlock requests. As a best practice, secret information such as passwords and PINs should be handled with the utmost care. Proper techniques for handling secret information within a credential provider are: 

                

<ul>
<li>Always securely discard secrets. To do this, call <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> before freeing the memory used to hold any secret.</li>
<li>Securely discard secrets promptly after they are used.</li>
<li>Securely discard secrets if they are not used for their intended purpose within an expected amount of time.</li>
</ul>