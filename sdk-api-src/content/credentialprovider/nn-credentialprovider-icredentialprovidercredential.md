---
UID: NN:credentialprovider.ICredentialProviderCredential
title: ICredentialProviderCredential (credentialprovider.h)
description: Exposes methods that enable the handling of a credential.
helpviewer_keywords: ["ICredentialProviderCredential","ICredentialProviderCredential interface [Windows Shell]","ICredentialProviderCredential interface [Windows Shell]","described","credentialprovider/ICredentialProviderCredential","shell.ICredentialProviderCredential","shell_ICredentialProviderCredential"]
old-location: shell\ICredentialProviderCredential.htm
tech.root: shell
ms.assetid: ef9bb148-0b4e-4c13-b69d-3e63a5592e4a
ms.date: 12/05/2018
ms.keywords: ICredentialProviderCredential, ICredentialProviderCredential interface [Windows Shell], ICredentialProviderCredential interface [Windows Shell],described, credentialprovider/ICredentialProviderCredential, shell.ICredentialProviderCredential, shell_ICredentialProviderCredential
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
 - ICredentialProviderCredential
 - credentialprovider/ICredentialProviderCredential
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
 - ICredentialProviderCredential
---

# ICredentialProviderCredential interface


## -description

Exposes methods that enable the handling of a credential.

## -inheritance

The <b>ICredentialProviderCredential</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICredentialProviderCredential</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
<b>ICredentialProviderCredential</b> is implemented by outside parties providing a Logon UI or Credential UI  prompting for user credentials. Enumeration of user tiles cannot be done without an implementation of this interface.

<h3><a id="Credential_Provider_Best_Practices"></a><a id="credential_provider_best_practices"></a><a id="CREDENTIAL_PROVIDER_BEST_PRACTICES"></a>Credential Provider Best Practices</h3>
Credential providers handle extremely sensitive user secrets in order to complete logon and unlock requests. As a best practice, secret information such as passwords and PINs should be handled with the utmost care. Proper techniques for handling secret information within a credential provider are: 

                

<ul>
<li>Always securely discard secrets. To do this, call <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> before freeing the memory used to hold any secret.</li>
<li>Securely discard secrets promptly after they are used.</li>
<li>Securely discard secrets if they are not used for their intended purpose within an expected amount of time.</li>
</ul>

## -see-also

<a href="/windows/desktop/SecAuthN/credential-providers-in-windows">Credential Providers in Windows 10</a>



<a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovider">ICredentialProvider</a>
