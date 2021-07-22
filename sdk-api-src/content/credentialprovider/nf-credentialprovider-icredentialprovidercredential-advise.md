---
UID: NF:credentialprovider.ICredentialProviderCredential.Advise
title: ICredentialProviderCredential::Advise (credentialprovider.h)
description: Enables a credential to initiate events in the Logon UI or Credential UI through a callback interface. This method should be called before other methods in ICredentialProviderCredential interface.
helpviewer_keywords: ["Advise","Advise method [Windows Shell]","Advise method [Windows Shell]","ICredentialProviderCredential interface","ICredentialProviderCredential interface [Windows Shell]","Advise method","ICredentialProviderCredential.Advise","ICredentialProviderCredential::Advise","credentialprovider/ICredentialProviderCredential::Advise","shell.ICredentialProviderCredential_Advise","shell_ICredentialProviderCredential_Advise"]
old-location: shell\ICredentialProviderCredential_Advise.htm
tech.root: shell
ms.assetid: 26db5ec5-78bf-4d88-90af-c822c8d3ce45
ms.date: 12/05/2018
ms.keywords: Advise, Advise method [Windows Shell], Advise method [Windows Shell],ICredentialProviderCredential interface, ICredentialProviderCredential interface [Windows Shell],Advise method, ICredentialProviderCredential.Advise, ICredentialProviderCredential::Advise, credentialprovider/ICredentialProviderCredential::Advise, shell.ICredentialProviderCredential_Advise, shell_ICredentialProviderCredential_Advise
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
 - ICredentialProviderCredential::Advise
 - credentialprovider/ICredentialProviderCredential::Advise
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
 - ICredentialProviderCredential.Advise
---

# ICredentialProviderCredential::Advise


## -description

Enables a credential to initiate events in the Logon UI or Credential UI through a callback interface. This method should be called before other methods in <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential">ICredentialProviderCredential</a> interface.

## -parameters

### -param pcpce [in]

Type: <b><a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents">ICredentialProviderCredentialEvents</a>*</b>

A pointer to an <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents">ICredentialProviderCredentialEvents</a> callback interface to be used as the notification mechanism.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is optional. If you do not implement this method, you should just return <b>E_NOTIMPL</b>.

Credential providers that implement this method have the responsibility of calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the provided <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents">ICredentialProviderCredentialEvents</a>. Those credential providers also need to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> during the <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-unadvise">UnAdvise</a> method.

## -see-also

<a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential">ICredentialProviderCredential</a>



<a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-unadvise">ICredentialProviderCredential::UnAdvise</a>