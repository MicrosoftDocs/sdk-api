---
UID: NN:subscriptionservices.IWMPSubscriptionService
title: IWMPSubscriptionService
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\iwmpsubscriptionservice.htm
old-project: WMP
ms.assetid: cb9d0f20-d5ca-4db9-adcc-0a803f97f196
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPSubscriptionService, IWMPSubscriptionService interface [Windows Media Player], IWMPSubscriptionService interface [Windows Media Player],described, IWMPSubscriptionServiceInterface, subscriptionservices/IWMPSubscriptionService, wmp.iwmpsubscriptionservice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: subscriptionservices.h
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
tech.root: 
req.typenames: WMPSubscriptionServiceEvent
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	subscriptionservices.h
api_name:
-	IWMPSubscriptionService
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IWMPSubscriptionService interface


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>IWMPSubscriptionService</b> interface provides methods to augment digital rights management (DRM) and initiate background processes when Windows Media Player opens premium content. These methods are implemented by the online store and called by Windows Media Player 9 Series or later.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPSubscriptionService</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPSubscriptionService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPSubscriptionService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a17ab1c3-8208-481f-8566-164e2d817e05">allowCDBurn</a>
</td>
<td align="left" width="63%">
Manages permission for Windows Media Player to copy content to a CD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a824c6c0-0887-41cb-892a-832635ade222">allowPDATransfer</a>
</td>
<td align="left" width="63%">
Manages permission for Windows Media Player to copy content to a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6350bf9d-f046-494f-8052-2a6f5339b4bd">allowPlay</a>
</td>
<td align="left" width="63%">
Manages permission for Windows Media Player to play content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3bdb4b1-8479-484f-92db-2b73a0c40bfb">startBackgroundProcessing</a>
</td>
<td align="left" width="63%">
Initiates background processing tasks.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b3f580cc-b02d-4312-a7a1-a35778a222bc">Reference for Type 2 Online Stores</a>
 

 

