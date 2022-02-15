---
UID: NF:credentialprovider.ICredentialProvider.UnAdvise
title: ICredentialProvider::UnAdvise (credentialprovider.h)
description: Used by the Logon UI or Credential UI to advise the credential provider that event callbacks are no longer accepted.
helpviewer_keywords: ["ICredentialProvider interface [Windows Shell]","UnAdvise method","ICredentialProvider.UnAdvise","ICredentialProvider::UnAdvise","UnAdvise","UnAdvise method [Windows Shell]","UnAdvise method [Windows Shell]","ICredentialProvider interface","credentialprovider/ICredentialProvider::UnAdvise","shell.ICredentialProvider_UnAdvise","shell_ICredentialProvider_UnAdvise"]
old-location: shell\ICredentialProvider_UnAdvise.htm
tech.root: shell
ms.assetid: d971c7be-f440-41ce-945d-4dbe51554e59
ms.date: 12/05/2018
ms.keywords: ICredentialProvider interface [Windows Shell],UnAdvise method, ICredentialProvider.UnAdvise, ICredentialProvider::UnAdvise, UnAdvise, UnAdvise method [Windows Shell], UnAdvise method [Windows Shell],ICredentialProvider interface, credentialprovider/ICredentialProvider::UnAdvise, shell.ICredentialProvider_UnAdvise, shell_ICredentialProvider_UnAdvise
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
 - ICredentialProvider::UnAdvise
 - credentialprovider/ICredentialProvider::UnAdvise
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
 - ICredentialProvider.UnAdvise
---

# ICredentialProvider::UnAdvise


## -description

Used by the Logon UI or Credential UI to advise the credential provider that event callbacks are no longer accepted.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method does not need to be implemented, and should return <b>E_NOTIMPL</b> if it does not. There might be no reason to call it, such as if the Logon UI or Credential UI never changes or updates.

If this method is called, it indicates that the <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialproviderevents">ICredentialProviderEvents</a> pointer provided in <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovider-advise">Advise</a> is no longer valid. It is the responsibility of the credential provider to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the provided <b>ICredentialProviderEvents</b> pointer during this method.

<div class="alert"><b>Important</b>  <p class="note">You should not use this method to clean up allocated memory for the credential provider. you should do that in the destructor of the credential provider as normal.

</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovider">ICredentialProvider</a>



<a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovider-advise">ICredentialProvider::Advise</a>
