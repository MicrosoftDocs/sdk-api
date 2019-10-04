---
UID: NN:subscriptionservices.IWMPSubscriptionService
title: IWMPSubscriptionService (subscriptionservices.h)
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\iwmpsubscriptionservice.htm
tech.root: WMP
ms.assetid: cb9d0f20-d5ca-4db9-adcc-0a803f97f196
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPSubscriptionService, IWMPSubscriptionService interface [Windows Media Player], IWMPSubscriptionService interface [Windows Media Player],described, IWMPSubscriptionServiceInterface, subscriptionservices/IWMPSubscriptionService, wmp.iwmpsubscriptionservice
ms.topic: interface
f1_keywords: 
 - "subscriptionservices/IWMPSubscriptionService"
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - subscriptionservices.h
api_name:
 - IWMPSubscriptionService
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPSubscriptionService interface


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>IWMPSubscriptionService</b> interface provides methods to augment digital rights management (DRM) and initiate background processes when Windows Media Player opens premium content. These methods are implemented by the online store and called by Windows Media Player 9 Series or later.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPSubscriptionService</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPSubscriptionService</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn">allowCDBurn</a>
</td>
<td align="left" width="63%">
Manages permission for Windows Media Player to copy content to a CD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowpdatransfer">allowPDATransfer</a>
</td>
<td align="left" width="63%">
Manages permission for Windows Media Player to copy content to a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay">allowPlay</a>
</td>
<td align="left" width="63%">
Manages permission for Windows Media Player to play content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing">startBackgroundProcessing</a>
</td>
<td align="left" width="63%">
Initiates background processing tasks.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/reference-for-type-2-online-stores">Reference for Type 2 Online Stores</a>
 

 

