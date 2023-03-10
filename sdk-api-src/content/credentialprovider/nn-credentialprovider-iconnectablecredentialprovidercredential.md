---
UID: NN:credentialprovider.IConnectableCredentialProviderCredential
title: IConnectableCredentialProviderCredential (credentialprovider.h)
description: Exposes methods for connecting and disconnecting IConnectableCredentialProviderCredential objects.
helpviewer_keywords: ["IConnectableCredentialProviderCredential","IConnectableCredentialProviderCredential interface [Windows Shell]","IConnectableCredentialProviderCredential interface [Windows Shell]","described","_shell_IConnectableCredentialProviderCredential","credentialprovider/IConnectableCredentialProviderCredential","shell.IConnectableCredentialProviderCredential"]
old-location: shell\IConnectableCredentialProviderCredential.htm
tech.root: shell
ms.assetid: fe5f3145-b428-42c9-ab1d-1c0e63c4454b
ms.date: 12/05/2018
ms.keywords: IConnectableCredentialProviderCredential, IConnectableCredentialProviderCredential interface [Windows Shell], IConnectableCredentialProviderCredential interface [Windows Shell],described, _shell_IConnectableCredentialProviderCredential, credentialprovider/IConnectableCredentialProviderCredential, shell.IConnectableCredentialProviderCredential
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
 - IConnectableCredentialProviderCredential
 - credentialprovider/IConnectableCredentialProviderCredential
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
 - IConnectableCredentialProviderCredential
---

# IConnectableCredentialProviderCredential interface


## -description

Exposes methods for connecting and disconnecting <b>IConnectableCredentialProviderCredential</b> objects.

## -inheritance

The <b>IConnectableCredentialProviderCredential</b> interface inherits from <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential">ICredentialProviderCredential</a>. <b>IConnectableCredentialProviderCredential</b> also has these types of members:

## -remarks

This interface is required for any credential provider that wants to connect to the network.

This interface also provides the methods of the <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential">ICredentialProviderCredential</a> interface, from which it inherits.

All tasks that might take an extended period of time, such as connecting to a network, should be handled with the <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-iconnectablecredentialprovidercredential-connect">Connect</a> method.
