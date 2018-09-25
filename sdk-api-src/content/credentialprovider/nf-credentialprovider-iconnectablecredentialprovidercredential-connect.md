---
UID: NF:credentialprovider.IConnectableCredentialProviderCredential.Connect
title: IConnectableCredentialProviderCredential::Connect
author: windows-sdk-content
description: Connects an IConnectableCredentialProviderCredential object. This method is called after the user clicks the Submit button within the Pre-Logon-Access Provider screen and before ICredentialProviderCredential::GetSerialization is called.
old-location: shell\IConnectableCredentialProviderCredential_Connect.htm
tech.root: shell
ms.assetid: 0fe91d1a-811a-4956-bb2f-47712ae2a155
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: Connect, Connect method [Windows Shell], Connect method [Windows Shell],IConnectableCredentialProviderCredential interface, IConnectableCredentialProviderCredential interface [Windows Shell],Connect method, IConnectableCredentialProviderCredential.Connect, IConnectableCredentialProviderCredential::Connect, _shell_IConnectableCredentialProviderCredential_Connect, credentialprovider/IConnectableCredentialProviderCredential::Connect, shell.IConnectableCredentialProviderCredential_Connect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IConnectableCredentialProviderCredential.Connect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConnectableCredentialProviderCredential::Connect


## -description


Connects an <a href="https://msdn.microsoft.com/fe5f3145-b428-42c9-ab1d-1c0e63c4454b">IConnectableCredentialProviderCredential</a> object. This method is called after the user clicks the <b>Submit</b> button within the Pre-Logon-Access Provider screen and before <a href="https://msdn.microsoft.com/c5f7ba25-c38a-431a-b4ad-0e2409f763a3">ICredentialProviderCredential::GetSerialization</a> is called.


## -parameters




### -param pqcws [in]

Type: <b><a href="https://msdn.microsoft.com/3f41714e-d8f6-46ea-aea4-19dca4723ca5">IQueryContinueWithStatus</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/3f41714e-d8f6-46ea-aea4-19dca4723ca5">IQueryContinueWithStatus</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 When Logon  UI calls this method, it passes a pointer to an <a href="https://msdn.microsoft.com/3f41714e-d8f6-46ea-aea4-19dca4723ca5">IQueryContinueWithStatus</a> instance. This object is used to query if the credential provider should continue attempt to connect to the network and to display status messages to the user while attempting to connect. Robust credential providers should periodically call <a href="https://msdn.microsoft.com/9beabfc9-56b9-4778-8027-939aa986086a">QueryContinue</a> during attempts to connect to a network to be able to respond to user input.

After a successful call to <b>Connect</b>, the Logon UI displays a <b>Disconnect</b> button to the user. If the user clicks <b>Disconnect</b>, the Logon UI calls <a href="https://msdn.microsoft.com/749147ce-9c05-4303-9ed2-62af047e6608">Disconnect</a> on every credential provider that implements <a href="https://msdn.microsoft.com/fe5f3145-b428-42c9-ab1d-1c0e63c4454b">IConnectableCredentialProviderCredential</a>.



