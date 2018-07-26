---
UID: NN:credentialprovider.IConnectableCredentialProviderCredential
title: IConnectableCredentialProviderCredential
author: windows-sdk-content
description: Exposes methods for connecting and disconnecting IConnectableCredentialProviderCredential objects.
old-location: shell\IConnectableCredentialProviderCredential.htm
old-project: shell
ms.assetid: fe5f3145-b428-42c9-ab1d-1c0e63c4454b
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IConnectableCredentialProviderCredential, IConnectableCredentialProviderCredential interface [Windows Shell], IConnectableCredentialProviderCredential interface [Windows Shell],described, _shell_IConnectableCredentialProviderCredential, credentialprovider/IConnectableCredentialProviderCredential, shell.IConnectableCredentialProviderCredential
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: CREDENTIAL_PROVIDER_USAGE_SCENARIO
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
req.lib: 
req.dll: 
req.irql: 
---

# IConnectableCredentialProviderCredential interface


## -description


Exposes methods for connecting and disconnecting <b>IConnectableCredentialProviderCredential</b> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConnectableCredentialProviderCredential</b> interface inherits from <a href="https://msdn.microsoft.com/ef9bb148-0b4e-4c13-b69d-3e63a5592e4a">ICredentialProviderCredential</a>. <b>IConnectableCredentialProviderCredential</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0fe91d1a-811a-4956-bb2f-47712ae2a155">Connect</a>
</td>
<td align="left" width="63%">
Connects an <b>IConnectableCredentialProviderCredential</b> object. This method is called after the user clicks the <b>Submit</b> button within the Pre-Logon-Access Provider screen and before <a href="https://msdn.microsoft.com/c5f7ba25-c38a-431a-b4ad-0e2409f763a3">ICredentialProviderCredential::GetSerialization</a> is called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/749147ce-9c05-4303-9ed2-62af047e6608">Disconnect</a>
</td>
<td align="left" width="63%">
Disconnects an <b>IConnectableCredentialProviderCredential</b> object.

</td>
</tr>
</table> 


## -remarks



This interface is required for any credential provider that wants to connect to the network.

This interface also provides the methods of the <a href="https://msdn.microsoft.com/ef9bb148-0b4e-4c13-b69d-3e63a5592e4a">ICredentialProviderCredential</a> interface, from which it inherits.

All tasks that might take an extended period of time, such as connecting to a network, should be handled with the <a href="https://msdn.microsoft.com/0fe91d1a-811a-4956-bb2f-47712ae2a155">Connect</a> method.



