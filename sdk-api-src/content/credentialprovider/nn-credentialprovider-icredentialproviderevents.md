---
UID: NN:credentialprovider.ICredentialProviderEvents
title: ICredentialProviderEvents
author: windows-sdk-content
description: Provides an asynchronous callback mechanism used by a credential provider to notify it of changes in the list of credentials or their fields.
old-location: shell\ICredentialProviderEvents.htm
tech.root: shell
ms.assetid: bf303b9d-2d6c-4de5-9bca-fc71d4f18903
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ICredentialProviderEvents, ICredentialProviderEvents interface [Windows Shell], ICredentialProviderEvents interface [Windows Shell],described, credentialprovider/ICredentialProviderEvents, shell.ICredentialProviderEvents, shell_ICredentialProviderEvents
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
 - ICredentialProviderEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICredentialProviderEvents interface


## -description


Provides an asynchronous callback mechanism used by a credential provider to notify it of changes in the list of credentials or their fields.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICredentialProviderEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICredentialProviderEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICredentialProviderEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bff835ed-01b9-4620-a97c-c64a2445e02a">CredentialsChanged</a>
</td>
<td align="left" width="63%">
Signals the Logon UI or Credential UI  that the enumerated list of credentials has changed.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
An implementation of <b>ICredentialProviderEvents</b> is provided for use by outside parties implementing a credential provider.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Outside parties do not need to implement <b>ICredentialProviderEvents</b> themselves.
            




## -see-also




<a href="https://msdn.microsoft.com/5ca35c90-24a3-4ffe-abf7-ba3ce0ec83b9">ICredentialProvider::Advise</a>



<a href="https://msdn.microsoft.com/d971c7be-f440-41ce-945d-4dbe51554e59">ICredentialProvider::UnAdvise</a>
 

 

