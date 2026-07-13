---
UID: NN:subscriptionservices.IWMPSubscriptionService
title: IWMPSubscriptionService (subscriptionservices.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["IWMPSubscriptionService","IWMPSubscriptionService interface [Windows Media Player]","IWMPSubscriptionService interface [Windows Media Player]","described","IWMPSubscriptionServiceInterface","subscriptionservices/IWMPSubscriptionService","wmp.iwmpsubscriptionservice"]
old-location: wmp\iwmpsubscriptionservice.htm
tech.root: WMP
ms.assetid: cb9d0f20-d5ca-4db9-adcc-0a803f97f196
ms.date: 4/26/2023
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

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

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
