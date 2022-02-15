---
UID: NN:credentialprovider.ICredentialProviderCredentialWithFieldOptions
title: ICredentialProviderCredentialWithFieldOptions (credentialprovider.h)
description: Provides a method that enables the credential provider framework to determine whether you've made a customization to a field's option in a logon or credential UI.
helpviewer_keywords: ["ICredentialProviderCredentialWithFieldOptions","ICredentialProviderCredentialWithFieldOptions interface [Windows Shell]","ICredentialProviderCredentialWithFieldOptions interface [Windows Shell]","described","credentialprovider/ICredentialProviderCredentialWithFieldOptions","shell.ICredentialProviderCredentialWithFieldOptions"]
old-location: shell\ICredentialProviderCredentialWithFieldOptions.htm
tech.root: shell
ms.assetid: 37C391D7-23C2-4053-BC7F-62F8AFD50DA3
ms.date: 12/05/2018
ms.keywords: ICredentialProviderCredentialWithFieldOptions, ICredentialProviderCredentialWithFieldOptions interface [Windows Shell], ICredentialProviderCredentialWithFieldOptions interface [Windows Shell],described, credentialprovider/ICredentialProviderCredentialWithFieldOptions, shell.ICredentialProviderCredentialWithFieldOptions
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
 - ICredentialProviderCredentialWithFieldOptions
 - credentialprovider/ICredentialProviderCredentialWithFieldOptions
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
 - ICredentialProviderCredentialWithFieldOptions
---

# ICredentialProviderCredentialWithFieldOptions interface


## -description

Provides a method that enables the credential provider framework to determine whether you've made a customization to a field's option in a logon or credential UI.

## -inheritance

The <b>ICredentialProviderCredentialWithFieldOptions</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICredentialProviderCredentialWithFieldOptions</b> also has these types of members:

## -remarks

<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
Implement this interface if your credential provider overrides the default field options through <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredentialevents2-setfieldoptions">ICredentialProviderCredentialEvents2::SetFieldOptions</a>. This enables the credential provider framework to determine the field options that you've specified .

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
