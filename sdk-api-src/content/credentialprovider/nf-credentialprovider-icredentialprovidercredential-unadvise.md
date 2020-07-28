---
UID: NF:credentialprovider.ICredentialProviderCredential.UnAdvise
title: ICredentialProviderCredential::UnAdvise (credentialprovider.h)
description: Used by the Logon UI or Credential UI to advise the credential that event callbacks are no longer accepted.
helpviewer_keywords: ["ICredentialProviderCredential interface [Windows Shell]","UnAdvise method","ICredentialProviderCredential.UnAdvise","ICredentialProviderCredential::UnAdvise","UnAdvise","UnAdvise method [Windows Shell]","UnAdvise method [Windows Shell]","ICredentialProviderCredential interface","credentialprovider/ICredentialProviderCredential::UnAdvise","shell.ICredentialProviderCredential_UnAdvise","shell_ICredentialProviderCredential_UnAdvise"]
old-location: shell\ICredentialProviderCredential_UnAdvise.htm
tech.root: shell
ms.assetid: 29e01ef4-3186-4f9a-9898-b7424bba2b61
ms.date: 12/05/2018
ms.keywords: ICredentialProviderCredential interface [Windows Shell],UnAdvise method, ICredentialProviderCredential.UnAdvise, ICredentialProviderCredential::UnAdvise, UnAdvise, UnAdvise method [Windows Shell], UnAdvise method [Windows Shell],ICredentialProviderCredential interface, credentialprovider/ICredentialProviderCredential::UnAdvise, shell.ICredentialProviderCredential_UnAdvise, shell_ICredentialProviderCredential_UnAdvise
f1_keywords:
- credentialprovider/ICredentialProviderCredential.UnAdvise
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Credentialprovider.h
api_name:
- ICredentialProviderCredential.UnAdvise
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICredentialProviderCredential::UnAdvise


## -description


Used by the Logon UI or Credential UI to advise the credential that event callbacks are no longer accepted.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is optional. If you do not implement this method, you should just return <b>E_NOTIMPL</b>.

If this method is called, it indicates that the <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents">ICredentialProviderCredentialEvents</a> pointer provided in <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-advise">Advise</a> is no longer valid. It is the responsibility of the credential provider to call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the provided <b>ICredentialProviderCredentialEvents</b> pointer during this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential">ICredentialProviderCredential</a>



<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-advise">ICredentialProviderCredential::Advise</a>
 

 

