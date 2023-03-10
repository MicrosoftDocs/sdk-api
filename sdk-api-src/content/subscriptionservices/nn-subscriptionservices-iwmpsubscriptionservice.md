---
UID: NN:subscriptionservices.IWMPSubscriptionService
title: IWMPSubscriptionService (subscriptionservices.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["IWMPSubscriptionService","IWMPSubscriptionService interface [Windows Media Player]","IWMPSubscriptionService interface [Windows Media Player]","described","IWMPSubscriptionServiceInterface","subscriptionservices/IWMPSubscriptionService","wmp.iwmpsubscriptionservice"]
old-location: wmp\iwmpsubscriptionservice.htm
tech.root: WMP
ms.assetid: cb9d0f20-d5ca-4db9-adcc-0a803f97f196
ms.date: 12/05/2018
ms.keywords: IWMPSubscriptionService, IWMPSubscriptionService interface [Windows Media Player], IWMPSubscriptionService interface [Windows Media Player],described, IWMPSubscriptionServiceInterface, subscriptionservices/IWMPSubscriptionService, wmp.iwmpsubscriptionservice
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPSubscriptionService
 - subscriptionservices/IWMPSubscriptionService
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - subscriptionservices.h
api_name:
 - IWMPSubscriptionService
---

# IWMPSubscriptionService interface


## -description

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>IWMPSubscriptionService</b> interface provides methods to augment digital rights management (DRM) and initiate background processes when Windows Media Player opens premium content. These methods are implemented by the online store and called by Windows Media Player 9 Series or later.

## -inheritance

The <b>IWMPSubscriptionService</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPSubscriptionService</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/WMP/reference-for-type-2-online-stores">Reference for Type 2 Online Stores</a>
