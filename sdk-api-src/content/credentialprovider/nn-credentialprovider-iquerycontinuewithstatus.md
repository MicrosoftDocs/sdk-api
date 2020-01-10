---
UID: NN:credentialprovider.IQueryContinueWithStatus
title: IQueryContinueWithStatus (credentialprovider.h)
description: Exposes methods that provide a standard mechanism for credential providers to call QueryContinue while attempting to connect to the network to determine if they should continue these attempts.
old-location: shell\IQueryContinueWithStatus.htm
tech.root: shell
ms.assetid: 3f41714e-d8f6-46ea-aea4-19dca4723ca5
ms.date: 12/05/2018
ms.keywords: IQueryContinueWithStatus, IQueryContinueWithStatus interface [Windows Shell], IQueryContinueWithStatus interface [Windows Shell],described, _shell_IQueryContinueWithStatus, credentialprovider/IQueryContinueWithStatus, shell.IQueryContinueWithStatus
f1_keywords:
- credentialprovider/IQueryContinueWithStatus
dev_langs:
- c++
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
- IQueryContinueWithStatus
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IQueryContinueWithStatus interface


## -description


Exposes methods that provide a standard mechanism for credential providers to call <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iquerycontinue-querycontinue">QueryContinue</a> while attempting to connect to the network to determine if they should continue these attempts. Credential providers can also use this interface to display messages to the user while attempting to establish a network connection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IQueryContinueWithStatus</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iquerycontinue">IQueryContinue</a>. <b>IQueryContinueWithStatus</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-iquerycontinuewithstatus-setstatusmessage">SetStatusMessage</a>
</td>
<td align="left" width="63%">
Enables the credential provider to pass status messages to the Logon UI as it attempts to complete <a href="https://docs.microsoft.com/windows/desktop/api/credentialprovider/nf-credentialprovider-iconnectablecredentialprovidercredential-connect">IConnectableCredentialProviderCredential::Connect</a>.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iquerycontinue">IQueryContinue</a> interface, from which it inherits.



