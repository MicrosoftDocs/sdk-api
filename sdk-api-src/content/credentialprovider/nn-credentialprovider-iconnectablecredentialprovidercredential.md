---
UID: NN:credentialprovider.IConnectableCredentialProviderCredential
title: IConnectableCredentialProviderCredential (credentialprovider.h)
author: windows-sdk-content
description: Exposes methods for connecting and disconnecting IConnectableCredentialProviderCredential objects.
old-location: shell\IConnectableCredentialProviderCredential.htm
tech.root: shell
ms.assetid: fe5f3145-b428-42c9-ab1d-1c0e63c4454b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IConnectableCredentialProviderCredential, IConnectableCredentialProviderCredential interface [Windows Shell], IConnectableCredentialProviderCredential interface [Windows Shell],described, _shell_IConnectableCredentialProviderCredential, credentialprovider/IConnectableCredentialProviderCredential, shell.IConnectableCredentialProviderCredential
ms.topic: interface
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
 - IConnectableCredentialProviderCredential
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IConnectableCredentialProviderCredential interface


## -description


Exposes methods for connecting and disconnecting <b>IConnectableCredentialProviderCredential</b> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConnectableCredentialProviderCredential</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential">ICredentialProviderCredential</a>. <b>IConnectableCredentialProviderCredential</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IConnectableCredentialProviderCredential</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-iconnectablecredentialprovidercredential-connect">Connect</a>
</td>
<td align="left" width="63%">
Connects an <b>IConnectableCredentialProviderCredential</b> object. This method is called after the user clicks the <b>Submit</b> button within the Pre-Logon-Access Provider screen and before <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-getserialization">ICredentialProviderCredential::GetSerialization</a> is called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-iconnectablecredentialprovidercredential-disconnect">Disconnect</a>
</td>
<td align="left" width="63%">
Disconnects an <b>IConnectableCredentialProviderCredential</b> object.

</td>
</tr>
</table> 


## -remarks



This interface is required for any credential provider that wants to connect to the network.

This interface also provides the methods of the <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential">ICredentialProviderCredential</a> interface, from which it inherits.

All tasks that might take an extended period of time, such as connecting to a network, should be handled with the <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-iconnectablecredentialprovidercredential-connect">Connect</a> method.



