---
UID: NN:credentialprovider.IQueryContinueWithStatus
title: IQueryContinueWithStatus
author: windows-sdk-content
description: Exposes methods that provide a standard mechanism for credential providers to call QueryContinue while attempting to connect to the network to determine if they should continue these attempts.
old-location: shell\IQueryContinueWithStatus.htm
old-project: shell
ms.assetid: 3f41714e-d8f6-46ea-aea4-19dca4723ca5
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IQueryContinueWithStatus, IQueryContinueWithStatus interface [Windows Shell], IQueryContinueWithStatus interface [Windows Shell],described, _shell_IQueryContinueWithStatus, credentialprovider/IQueryContinueWithStatus, shell.IQueryContinueWithStatus
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
 - IQueryContinueWithStatus
product: Windows
targetos: Windows
req.lib: CredentialProvider.lib
req.dll: Authui.dll
req.irql: 
---

# IQueryContinueWithStatus interface


## -description


Exposes methods that provide a standard mechanism for credential providers to call <a href="https://msdn.microsoft.com/9beabfc9-56b9-4778-8027-939aa986086a">QueryContinue</a> while attempting to connect to the network to determine if they should continue these attempts. Credential providers can also use this interface to display messages to the user while attempting to establish a network connection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IQueryContinueWithStatus</b> interface inherits from <a href="https://msdn.microsoft.com/94dee6cc-a142-4180-a562-14f4ded16884">IQueryContinue</a>. <b>IQueryContinueWithStatus</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IQueryContinueWithStatus</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1619c592-f79b-429f-a1dc-ce0b66542dd6">SetStatusMessage</a>
</td>
<td align="left" width="63%">
Enables the credential provider to pass status messages to the Logon UI as it attempts to complete <a href="https://msdn.microsoft.com/0fe91d1a-811a-4956-bb2f-47712ae2a155">IConnectableCredentialProviderCredential::Connect</a>.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/94dee6cc-a142-4180-a562-14f4ded16884">IQueryContinue</a> interface, from which it inherits.



