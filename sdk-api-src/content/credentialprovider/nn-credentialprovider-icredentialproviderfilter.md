---
UID: NN:credentialprovider.ICredentialProviderFilter
title: ICredentialProviderFilter
author: windows-sdk-content
description: Used to dynamically filter credential providers based on information available at runtime.
old-location: shell\ICredentialProviderFilter.htm
tech.root: shell
ms.assetid: a12a0648-ea60-4537-9d5c-8d21fd53cc80
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICredentialProviderFilter, ICredentialProviderFilter interface [Windows Shell], ICredentialProviderFilter interface [Windows Shell],described, _shell_ICredentialProviderFilter, credentialprovider/ICredentialProviderFilter, shell.ICredentialProviderFilter
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
 - ICredentialProviderFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICredentialProviderFilter interface


## -description


Used to dynamically filter credential providers based on information available at runtime.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICredentialProviderFilter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICredentialProviderFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICredentialProviderFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ba60965-6f18-427f-851d-b92c71eb03d2">Filter</a>
</td>
<td align="left" width="63%">
Evaluates whether a list of credential providers should be allowed to provide credential tiles.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0730f67-e4f1-42b2-823a-75b08a5c952e">UpdateRemoteCredential</a>
</td>
<td align="left" width="63%">
Updates a credential from a remote session.

</td>
</tr>
</table> 


## -remarks



It is recommended that third party credential providers do not use this interface to filter or disable system credential providers on a desktop. If an enterprise deploys a third party credential provider and wants to disable system credential providers currently available, that is a decision that should be made by a domain administrator after careful consideration. System policies exist that enable administrators to filter out credential providers and those should be used instead of building filters directly into a third party credential provider.



