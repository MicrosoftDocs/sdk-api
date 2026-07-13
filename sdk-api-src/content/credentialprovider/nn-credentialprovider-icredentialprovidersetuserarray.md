---
UID: NN:credentialprovider.ICredentialProviderSetUserArray
title: ICredentialProviderSetUserArray (credentialprovider.h)
description: Provides a method that enables a credential provider to receive the set of users that will be shown in the logon or credential UI.
helpviewer_keywords: ["ICredentialProviderSetUserArray","ICredentialProviderSetUserArray interface [Windows Shell]","ICredentialProviderSetUserArray interface [Windows Shell]","described","credentialprovider/ICredentialProviderSetUserArray","shell.ICredentialProviderSetUserArray"]
old-location: shell\ICredentialProviderSetUserArray.htm
tech.root: shell
ms.assetid: 85422EF5-8A8E-4e14-BD32-953C31A9D401
ms.date: 12/05/2018
ms.keywords: ICredentialProviderSetUserArray, ICredentialProviderSetUserArray interface [Windows Shell], ICredentialProviderSetUserArray interface [Windows Shell],described, credentialprovider/ICredentialProviderSetUserArray, shell.ICredentialProviderSetUserArray
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
 - ICredentialProviderSetUserArray
 - credentialprovider/ICredentialProviderSetUserArray
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
 - ICredentialProviderSetUserArray
---

# ICredentialProviderSetUserArray interface


## -description

Provides a method that enables a credential provider to receive the set of users that will be shown in the logon or credential UI.

## -inheritance

The <b>ICredentialProviderSetUserArray</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICredentialProviderSetUserArray</b> also has these types of members:

## -remarks

<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
Implement this interface for credential providers that have a need to know which users will appear in the logon or credential UI.

<h3><a id="When_to_use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to use</h3>
This interface is used only by the Windows credential provider framework. Its method should not be called by other parties.

## -see-also

<a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovideruserarray">ICredentialProviderUserArray</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
