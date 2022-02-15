---
UID: NN:credentialprovider.ICredentialProviderCredentialEvents
title: ICredentialProviderCredentialEvents (credentialprovider.h)
description: Provides an asynchronous callback mechanism used by a credential to notify it of state or text change events in the Logon UI or Credential UI.
helpviewer_keywords: ["ICredentialProviderCredentialEvents","ICredentialProviderCredentialEvents interface [Windows Shell]","ICredentialProviderCredentialEvents interface [Windows Shell]","described","credentialprovider/ICredentialProviderCredentialEvents","shell.ICredentialProviderCredentialEvents","shell_ICredentialProviderCredentialEvents"]
old-location: shell\ICredentialProviderCredentialEvents.htm
tech.root: shell
ms.assetid: 258449a4-78e2-475e-ab16-6481207e7354
ms.date: 12/05/2018
ms.keywords: ICredentialProviderCredentialEvents, ICredentialProviderCredentialEvents interface [Windows Shell], ICredentialProviderCredentialEvents interface [Windows Shell],described, credentialprovider/ICredentialProviderCredentialEvents, shell.ICredentialProviderCredentialEvents, shell_ICredentialProviderCredentialEvents
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
req.lib: CredentialProvider.lib
req.dll: Authui.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICredentialProviderCredentialEvents
 - credentialprovider/ICredentialProviderCredentialEvents
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Authui.dll
api_name:
 - ICredentialProviderCredentialEvents
---

# ICredentialProviderCredentialEvents interface


## -description

Provides an asynchronous callback mechanism used by a credential to notify it of state or text change events in the Logon UI or Credential UI.

## -inheritance

The <b>ICredentialProviderCredentialEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICredentialProviderCredentialEvents</b> also has these types of members:

## -remarks

These methods should only be called by a credential passing <b>this</b> as the first parameter. Behavior is undefined if you attempt to call these methods using a credential other than the one activated by the call on <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-advise">Advise</a>. If a credential provider has information on another thread and wants to communicate through that thread's Logon UI or Credential UI, the requests will need to go through the credential that received the <b>Advise</b> call.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Third parties do not implement <b>ICredentialProviderCredentialEvents</b>. An implementation is included with Windows.

## -see-also

<a href="/windows/desktop/SecAuthN/credential-providers-in-windows">Credential Providers in Windows 10</a>



<a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-advise">ICredentialProviderCredential::Advise</a>



<a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-unadvise">ICredentialProviderCredential::UnAdvise</a>



<a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents2">ICredentialProviderCredentialEvents2</a>
