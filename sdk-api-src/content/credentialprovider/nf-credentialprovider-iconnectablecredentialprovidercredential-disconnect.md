---
UID: NF:credentialprovider.IConnectableCredentialProviderCredential.Disconnect
title: IConnectableCredentialProviderCredential::Disconnect (credentialprovider.h)
description: Disconnects an IConnectableCredentialProviderCredential object.
helpviewer_keywords: ["Disconnect","Disconnect method [Windows Shell]","Disconnect method [Windows Shell]","IConnectableCredentialProviderCredential interface","IConnectableCredentialProviderCredential interface [Windows Shell]","Disconnect method","IConnectableCredentialProviderCredential.Disconnect","IConnectableCredentialProviderCredential::Disconnect","_shell_IConnectableCredentialProviderCredential_Disconnect","credentialprovider/IConnectableCredentialProviderCredential::Disconnect","shell.IConnectableCredentialProviderCredential_Disconnect"]
old-location: shell\IConnectableCredentialProviderCredential_Disconnect.htm
tech.root: shell
ms.assetid: 749147ce-9c05-4303-9ed2-62af047e6608
ms.date: 12/05/2018
ms.keywords: Disconnect, Disconnect method [Windows Shell], Disconnect method [Windows Shell],IConnectableCredentialProviderCredential interface, IConnectableCredentialProviderCredential interface [Windows Shell],Disconnect method, IConnectableCredentialProviderCredential.Disconnect, IConnectableCredentialProviderCredential::Disconnect, _shell_IConnectableCredentialProviderCredential_Disconnect, credentialprovider/IConnectableCredentialProviderCredential::Disconnect, shell.IConnectableCredentialProviderCredential_Disconnect
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
 - IConnectableCredentialProviderCredential::Disconnect
 - credentialprovider/IConnectableCredentialProviderCredential::Disconnect
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
 - IConnectableCredentialProviderCredential.Disconnect
---

# IConnectableCredentialProviderCredential::Disconnect


## -description

Disconnects an <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-iconnectablecredentialprovidercredential">IConnectableCredentialProviderCredential</a> object.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

After a successful call to <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-iconnectablecredentialprovidercredential-connect">Connect</a>, the Logon UI displays a <b>Disconnect</b> button to the user. If the user clicks <b>Disconnect</b>, the Logon UI calls <b>Disconnect</b> on every credential provider that implements <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-iconnectablecredentialprovidercredential">IConnectableCredentialProviderCredential</a>.
