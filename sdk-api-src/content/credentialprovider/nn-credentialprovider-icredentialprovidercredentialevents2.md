---
UID: NN:credentialprovider.ICredentialProviderCredentialEvents2
title: ICredentialProviderCredentialEvents2 (credentialprovider.h)
description: Extends the ICredentialProviderCredentialEvents interface by adding methods that enable batch updating of fields in theLogon UI or Credential UI.
helpviewer_keywords: ["ICredentialProviderCredentialEvents2","ICredentialProviderCredentialEvents2 interface [Windows Shell]","ICredentialProviderCredentialEvents2 interface [Windows Shell]","described","credentialprovider/ICredentialProviderCredentialEvents2","shell.ICredentialProviderCredentialEvents2"]
old-location: shell\ICredentialProviderCredentialEvents2.htm
tech.root: shell
ms.assetid: 47290FF7-1785-4470-B3A9-F35C5028A6FE
ms.date: 12/05/2018
ms.keywords: ICredentialProviderCredentialEvents2, ICredentialProviderCredentialEvents2 interface [Windows Shell], ICredentialProviderCredentialEvents2 interface [Windows Shell],described, credentialprovider/ICredentialProviderCredentialEvents2, shell.ICredentialProviderCredentialEvents2
req.header: credentialprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CredentialProvider.idl
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
 - ICredentialProviderCredentialEvents2
 - credentialprovider/ICredentialProviderCredentialEvents2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CredentialProvider.h
api_name:
 - ICredentialProviderCredentialEvents2
---

# ICredentialProviderCredentialEvents2 interface


## -description

Extends the <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents">ICredentialProviderCredentialEvents</a> interface by adding methods that enable batch updating of fields in theLogon UI or Credential UI.

## -inheritance

The <b>ICredentialProviderCredentialEvents2</b> interface inherits from <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents">ICredentialProviderCredentialEvents</a>. <b>ICredentialProviderCredentialEvents2</b> also has these types of members:

## -remarks

In Windows 7 and Windows Vista, many credential providers used <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialproviderevents-credentialschanged">ICredentialProviderEvents::CredentialsChanged</a> to update UI. While this works, it causes a re-enumeration of all the credentials from the calling credential provider. The processing of this event can, under some circumstances, lead to flashing or focus changes in the UI due to this re-enumeration. Therefore, using <b>ICredentialProviderEvents::CredentialsChanged</b> solely for UI updates is discouraged. The new recommendation is as follows:

                

<ul>
<li>Use <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialproviderevents-credentialschanged">ICredentialProviderEvents::CredentialsChanged</a> only if a credential provider needs to do automatically logon a user or change the number of credentials it is enumerating.</li>
<li>Use <b>ICredentialProviderCredentialEvents2</b> to update a credential provider's UI.</li>
</ul>
<b>ICredentialProviderCredentialEvents2</b> includes all of the methods inherited from <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents">ICredentialProviderCredentialEvents</a>. This includes all of the inherited methods except <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents-oncreatingwindow">OnCreatingWindow</a>.

When interacting with a background thread, the use of <b>ICredentialProviderCredentialEvents2</b> is similar to the use of <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents">ICredentialProviderCredentialEvents</a>, in that proper inter-thread communication methods must be used.

<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
Third-parties do not implement this interface. Call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method on <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents">ICredentialProviderCredentialEvents</a> to obtain this object.

## -see-also

<a href="/windows/desktop/SecAuthN/credential-providers-in-windows">Credential Providers in Windows 10</a>



<a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents">ICredentialProviderCredentialEvents</a>
