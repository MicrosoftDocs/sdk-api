---
UID: NF:credentialprovider.ICredentialProvider.Advise
title: ICredentialProvider::Advise (credentialprovider.h)
description: Allows a credential provider to initiate events in the Logon UI or Credential UI through a callback interface.
helpviewer_keywords: ["Advise","Advise method [Windows Shell]","Advise method [Windows Shell]","ICredentialProvider interface","ICredentialProvider interface [Windows Shell]","Advise method","ICredentialProvider.Advise","ICredentialProvider::Advise","credentialprovider/ICredentialProvider::Advise","shell.ICredentialProvider_Advise","shell_ICredentialProvider_Advise"]
old-location: shell\ICredentialProvider_Advise.htm
tech.root: shell
ms.assetid: 5ca35c90-24a3-4ffe-abf7-ba3ce0ec83b9
ms.date: 12/05/2018
ms.keywords: Advise, Advise method [Windows Shell], Advise method [Windows Shell],ICredentialProvider interface, ICredentialProvider interface [Windows Shell],Advise method, ICredentialProvider.Advise, ICredentialProvider::Advise, credentialprovider/ICredentialProvider::Advise, shell.ICredentialProvider_Advise, shell_ICredentialProvider_Advise
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
 - ICredentialProvider::Advise
 - credentialprovider/ICredentialProvider::Advise
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
 - ICredentialProvider.Advise
---

# ICredentialProvider::Advise


## -description

Allows a credential provider to initiate events in the Logon UI or Credential UI through a callback interface.

## -parameters

### -param pcpe [in]

Type: <b><a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialproviderevents">ICredentialProviderEvents</a>*</b>

A pointer to an <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialproviderevents">ICredentialProviderEvents</a> callback interface to be used as the notification mechanism.

### -param upAdviseContext [in]

Type: <b>UINT_PTR</b>

A pointer to an integer that uniquely identifies which credential provider has requested re-enumeration.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The method does not need to be implemented, and should return <b>E_NOTIMPL</b> if it doesn't. There might be no reason to call it, such as if the Logon UI or Credential UI never changes or updates.

This method enables the Logon UI and the Credential UI to pass an <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialproviderevents">ICredentialProviderEvents</a> pointer to the credential provider. This enables the credential provider to have asynchronous callback communication with the Logon or Credential UI. For example, a smart card provider might want to enumerate credentials again when a new smart card is inserted. In order to trigger the Logon UI to get credentials again,  the credential provider should call <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialproviderevents-credentialschanged">CredentialsChanged</a> providing the <i>upAdviseContext</i> identifier.

Credential providers that implement this method have the responsibility of calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the provided <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialproviderevents">ICredentialProviderEvents</a>. Those credential providers also need to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> during the <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovider-unadvise">UnAdvise</a> method.

## -see-also

<a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovider">ICredentialProvider</a>



<a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovider-unadvise">ICredentialProvider::UnAdvise</a>