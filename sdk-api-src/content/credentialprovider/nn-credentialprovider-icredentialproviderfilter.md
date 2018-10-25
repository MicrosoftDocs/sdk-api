---
UID: NN:credentialprovider.ICredentialProviderFilter
title: ICredentialProviderFilter
author: windows-sdk-content
description: Used to dynamically filter credential providers based on information available at runtime.
old-location: shell\ICredentialProviderFilter.htm
tech.root: shell
ms.assetid: a12a0648-ea60-4537-9d5c-8d21fd53cc80
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ICredentialProviderFilter, ICredentialProviderFilter interface [Windows Shell], ICredentialProviderFilter interface [Windows Shell],described, _shell_ICredentialProviderFilter, credentialprovider/ICredentialProviderFilter, shell.ICredentialProviderFilter
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICredentialProviderFilter</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ICredentialProviderFilter</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Bb776003(v=VS.85).aspx">Filter</a>
</td>
<td align="left" width="63%">
Evaluates whether a list of credential providers should be allowed to provide credential tiles.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb776005(v=VS.85).aspx">UpdateRemoteCredential</a>
</td>
<td align="left" width="63%">
Updates a credential from a remote session.

</td>
</tr>
</table> 


## -remarks



It is recommended that third party credential providers do not use this interface to filter or disable system credential providers on a desktop. If an enterprise deploys a third party credential provider and wants to disable system credential providers currently available, that is a decision that should be made by a domain administrator after careful consideration. System policies exist that enable administrators to filter out credential providers and those should be used instead of building filters directly into a third party credential provider.



