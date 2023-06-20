---
UID: NN:subscriptionservices.IWMPSubscriptionService2
title: IWMPSubscriptionService2 (subscriptionservices.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["IWMPSubscriptionService2","IWMPSubscriptionService2 interface [Windows Media Player]","IWMPSubscriptionService2 interface [Windows Media Player]","described","IWMPSubscriptionService2Interface","subscriptionservices/IWMPSubscriptionService2","wmp.iwmpsubscriptionservice2"]
old-location: wmp\iwmpsubscriptionservice2.htm
tech.root: WMP
ms.assetid: 5338a3c1-c44a-4c03-a21a-6cd5cfeef064
ms.date: 4/26/2023
ms.keywords: IWMPSubscriptionService2, IWMPSubscriptionService2 interface [Windows Media Player], IWMPSubscriptionService2 interface [Windows Media Player],described, IWMPSubscriptionService2Interface, subscriptionservices/IWMPSubscriptionService2, wmp.iwmpsubscriptionservice2
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
 - IWMPSubscriptionService2
 - subscriptionservices/IWMPSubscriptionService2
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
 - IWMPSubscriptionService2
---

# IWMPSubscriptionService2 interface


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>IWMPSubscriptionService2</b> interface extends <b>IWMPSubscriptionService</b>. It provides methods to initiate background processes, to provide notifications about online store activity, and to provide a pointer to the Windows Media Player core interface. These methods are implemented by the online store and called by Windows Media Player 10 or later.

## -inheritance

The <b>IWMPSubscriptionService2</b> interface inherits from <a href="/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice">IWMPSubscriptionService</a>. <b>IWMPSubscriptionService2</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice">IWMPSubscriptionService</a>



<a href="/windows/desktop/WMP/reference-for-type-2-online-stores">Reference for Type 2 Online Stores</a>
