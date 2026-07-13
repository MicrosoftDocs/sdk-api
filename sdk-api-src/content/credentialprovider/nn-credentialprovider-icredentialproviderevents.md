---
UID: NN:credentialprovider.ICredentialProviderEvents
title: ICredentialProviderEvents (credentialprovider.h)
description: Provides an asynchronous callback mechanism used by a credential provider to notify it of changes in the list of credentials or their fields.
helpviewer_keywords: ["ICredentialProviderEvents","ICredentialProviderEvents interface [Windows Shell]","ICredentialProviderEvents interface [Windows Shell]","described","credentialprovider/ICredentialProviderEvents","shell.ICredentialProviderEvents","shell_ICredentialProviderEvents"]
old-location: shell\ICredentialProviderEvents.htm
tech.root: shell
ms.assetid: bf303b9d-2d6c-4de5-9bca-fc71d4f18903
ms.date: 12/05/2018
ms.keywords: ICredentialProviderEvents, ICredentialProviderEvents interface [Windows Shell], ICredentialProviderEvents interface [Windows Shell],described, credentialprovider/ICredentialProviderEvents, shell.ICredentialProviderEvents, shell_ICredentialProviderEvents
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
 - ICredentialProviderEvents
 - credentialprovider/ICredentialProviderEvents
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
 - ICredentialProviderEvents
---

# ICredentialProviderEvents interface


## -description

Provides an asynchronous callback mechanism used by a credential provider to notify it of changes in the list of credentials or their fields.

## -inheritance

The <b>ICredentialProviderEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICredentialProviderEvents</b> also has these types of members:

## -remarks

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
An implementation of <b>ICredentialProviderEvents</b> is provided for use by outside parties implementing a credential provider.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Outside parties do not need to implement <b>ICredentialProviderEvents</b> themselves.

## -see-also

<a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovider-advise">ICredentialProvider::Advise</a>



<a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovider-unadvise">ICredentialProvider::UnAdvise</a>
