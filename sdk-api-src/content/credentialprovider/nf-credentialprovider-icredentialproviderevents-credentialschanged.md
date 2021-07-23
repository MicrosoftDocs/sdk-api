---
UID: NF:credentialprovider.ICredentialProviderEvents.CredentialsChanged
title: ICredentialProviderEvents::CredentialsChanged (credentialprovider.h)
description: Signals the Logon UI or Credential UI that the enumerated list of credentials has changed.
helpviewer_keywords: ["CredentialsChanged","CredentialsChanged method [Windows Shell]","CredentialsChanged method [Windows Shell]","ICredentialProviderEvents interface","ICredentialProviderEvents interface [Windows Shell]","CredentialsChanged method","ICredentialProviderEvents.CredentialsChanged","ICredentialProviderEvents::CredentialsChanged","credentialprovider/ICredentialProviderEvents::CredentialsChanged","shell.ICredentialProviderEvents_CredentialsChanged","shell_ICredentialProviderEvents_CredentialsChanged"]
old-location: shell\ICredentialProviderEvents_CredentialsChanged.htm
tech.root: shell
ms.assetid: bff835ed-01b9-4620-a97c-c64a2445e02a
ms.date: 12/05/2018
ms.keywords: CredentialsChanged, CredentialsChanged method [Windows Shell], CredentialsChanged method [Windows Shell],ICredentialProviderEvents interface, ICredentialProviderEvents interface [Windows Shell],CredentialsChanged method, ICredentialProviderEvents.CredentialsChanged, ICredentialProviderEvents::CredentialsChanged, credentialprovider/ICredentialProviderEvents::CredentialsChanged, shell.ICredentialProviderEvents_CredentialsChanged, shell_ICredentialProviderEvents_CredentialsChanged
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
 - ICredentialProviderEvents::CredentialsChanged
 - credentialprovider/ICredentialProviderEvents::CredentialsChanged
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
 - ICredentialProviderEvents.CredentialsChanged
---

# ICredentialProviderEvents::CredentialsChanged


## -description

Signals the Logon UI or Credential UI that the enumerated list of credentials has changed. This happens when the number of credentials change, the individual credentials change, or the number of fields available change. This is an asynchronous method.

## -parameters

### -param upAdviseContext [in]

Type: <b>UINT_PTR</b>

A pointer to an integer that uniquely identifies which credential provider has requested re-enumeration. The credential provider should pass back the interface pointer it received from <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovider-advise">Advise</a> in this parameter.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

In the past, many credential providers used <b>ICredentialProviderEvents::CredentialsChanged</b> to update UI. While this works, it causes a re-enumeration of all the credentials from the calling credential provider. The processing of this event can, under some circumstances, lead to flashing or focus changes in the UI due to this re-enumeration. Therefore, using <b>ICredentialProviderEvents::CredentialsChanged</b> solely for UI updates is discouraged. The new recommendation is as follows:

                

<ul>
<li>Use <b>ICredentialProviderEvents::CredentialsChanged</b> only if a credential provider needs to do an auto logon or change the number of credentials it is enumerating.</li>
<li>Use <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents2">ICredentialProviderCredentialEvents2</a> to update a credential provider's Logon UI or Credential UI.</li>
</ul>