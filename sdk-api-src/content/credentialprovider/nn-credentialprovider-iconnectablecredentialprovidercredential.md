---
UID: NN:credentialprovider.IConnectableCredentialProviderCredential
title: IConnectableCredentialProviderCredential
author: windows-sdk-content
description: Exposes methods for connecting and disconnecting IConnectableCredentialProviderCredential objects.
old-location: shell\IConnectableCredentialProviderCredential.htm
old-project: shell
ms.assetid: fe5f3145-b428-42c9-ab1d-1c0e63c4454b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IConnectableCredentialProviderCredential, IConnectableCredentialProviderCredential interface [Windows Shell], IConnectableCredentialProviderCredential interface [Windows Shell],described, _shell_IConnectableCredentialProviderCredential, credentialprovider/IConnectableCredentialProviderCredential, shell.IConnectableCredentialProviderCredential
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: credentialprovider.h
req.include-header: 
req.redist: 
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConnectableCredentialProviderCredential</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb776029(v=VS.85).aspx">ICredentialProviderCredential</a>. <b>IConnectableCredentialProviderCredential</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Bb776100(v=VS.85).aspx">Connect</a>
</td>
<td align="left" width="63%">
Connects an <b>IConnectableCredentialProviderCredential</b> object. This method is called after the user clicks the <b>Submit</b> button within the Pre-Logon-Access Provider screen and before <a href="https://msdn.microsoft.com/en-us/library/Bb776026(v=VS.85).aspx">ICredentialProviderCredential::GetSerialization</a> is called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb776101(v=VS.85).aspx">Disconnect</a>
</td>
<td align="left" width="63%">
Disconnects an <b>IConnectableCredentialProviderCredential</b> object.

</td>
</tr>
</table> 


## -remarks



This interface is required for any credential provider that wants to connect to the network.

This interface also provides the methods of the <a href="https://msdn.microsoft.com/en-us/library/Bb776029(v=VS.85).aspx">ICredentialProviderCredential</a> interface, from which it inherits.

All tasks that might take an extended period of time, such as connecting to a network, should be handled with the <a href="https://msdn.microsoft.com/en-us/library/Bb776100(v=VS.85).aspx">Connect</a> method.



