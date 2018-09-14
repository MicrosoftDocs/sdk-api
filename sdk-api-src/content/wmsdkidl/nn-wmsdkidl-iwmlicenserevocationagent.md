---
UID: NN:wmsdkidl.IWMLicenseRevocationAgent
title: IWMLicenseRevocationAgent
author: windows-sdk-content
description: The IWMLicenseRevocationAgent interface handles messages from a DRM license server that involve license revocation.IWMLicenseRevocationAgent is the primary interface of the license revocation agent object.
old-location: wmformat\iwmlicenserevocationagent.htm
tech.root: wmformat
ms.assetid: 4cb5beb9-72b8-46cb-8460-56455785a7a0
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWMLicenseRevocationAgent, IWMLicenseRevocationAgent interface [windows Media Format], IWMLicenseRevocationAgent interface [windows Media Format],described, IWMLicenseRevocationAgentInterface, wmformat.iwmlicenserevocationagent, wmsdkidl/IWMLicenseRevocationAgent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - wmsdkidl.h
api_name:
 - IWMLicenseRevocationAgent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMLicenseRevocationAgent interface


## -description



The <b>IWMLicenseRevocationAgent</b> interface handles messages from a DRM license server that involve license revocation.

<b>IWMLicenseRevocationAgent</b> is the primary interface of the license revocation agent object. You can create an instance of the object and retrieve a pointer to its <b>IWMLicenseRevocationAgent</b> interface by calling the <a href="https://msdn.microsoft.com/46898846-780f-4a86-93c7-826f55c358ba">WMCreateLicenseRevocationAgent</a> function.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMLicenseRevocationAgent</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMLicenseRevocationAgent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMLicenseRevocationAgent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9006f6c5-f9e7-4d00-a7c2-bbdfcfdd85e7">GetLRBChallenge</a>
</td>
<td align="left" width="63%">
Generates a response to a license revocation challenge message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/185611f8-beef-47b8-a9c2-abcda7651a18">ProcessLRB</a>
</td>
<td align="left" width="63%">
Performs license revocation.

</td>
</tr>
</table> 


## -remarks



License revocation enables a license issuer to remove licenses from a computer.




## -see-also




<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>
 

 

