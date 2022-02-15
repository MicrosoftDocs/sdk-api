---
UID: NF:credentialprovider.IConnectableCredentialProviderCredential.Connect
title: IConnectableCredentialProviderCredential::Connect (credentialprovider.h)
description: Connects an IConnectableCredentialProviderCredential object. This method is called after the user clicks the Submit button within the Pre-Logon-Access Provider screen and before ICredentialProviderCredential::GetSerialization is called.
helpviewer_keywords: ["Connect","Connect method [Windows Shell]","Connect method [Windows Shell]","IConnectableCredentialProviderCredential interface","IConnectableCredentialProviderCredential interface [Windows Shell]","Connect method","IConnectableCredentialProviderCredential.Connect","IConnectableCredentialProviderCredential::Connect","_shell_IConnectableCredentialProviderCredential_Connect","credentialprovider/IConnectableCredentialProviderCredential::Connect","shell.IConnectableCredentialProviderCredential_Connect"]
old-location: shell\IConnectableCredentialProviderCredential_Connect.htm
tech.root: shell
ms.assetid: 0fe91d1a-811a-4956-bb2f-47712ae2a155
ms.date: 12/05/2018
ms.keywords: Connect, Connect method [Windows Shell], Connect method [Windows Shell],IConnectableCredentialProviderCredential interface, IConnectableCredentialProviderCredential interface [Windows Shell],Connect method, IConnectableCredentialProviderCredential.Connect, IConnectableCredentialProviderCredential::Connect, _shell_IConnectableCredentialProviderCredential_Connect, credentialprovider/IConnectableCredentialProviderCredential::Connect, shell.IConnectableCredentialProviderCredential_Connect
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
 - IConnectableCredentialProviderCredential::Connect
 - credentialprovider/IConnectableCredentialProviderCredential::Connect
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
 - IConnectableCredentialProviderCredential.Connect
---

# IConnectableCredentialProviderCredential::Connect


## -description

Connects an <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-iconnectablecredentialprovidercredential">IConnectableCredentialProviderCredential</a> object. This method is called after the user clicks the <b>Submit</b> button within the Pre-Logon-Access Provider screen and before <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-getserialization">ICredentialProviderCredential::GetSerialization</a> is called.

## -parameters

### -param pqcws [in]

Type: <b><a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-iquerycontinuewithstatus">IQueryContinueWithStatus</a>*</b>

A pointer to an <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-iquerycontinuewithstatus">IQueryContinueWithStatus</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 When Logon  UI calls this method, it passes a pointer to an <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-iquerycontinuewithstatus">IQueryContinueWithStatus</a> instance. This object is used to query if the credential provider should continue attempt to connect to the network and to display status messages to the user while attempting to connect. Robust credential providers should periodically call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iquerycontinue-querycontinue">QueryContinue</a> during attempts to connect to a network to be able to respond to user input.

After a successful call to <b>Connect</b>, the Logon UI displays a <b>Disconnect</b> button to the user. If the user clicks <b>Disconnect</b>, the Logon UI calls <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-iconnectablecredentialprovidercredential-disconnect">Disconnect</a> on every credential provider that implements <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-iconnectablecredentialprovidercredential">IConnectableCredentialProviderCredential</a>.