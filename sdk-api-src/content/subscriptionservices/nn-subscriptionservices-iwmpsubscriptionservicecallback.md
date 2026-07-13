---
UID: NN:subscriptionservices.IWMPSubscriptionServiceCallback
title: IWMPSubscriptionServiceCallback (subscriptionservices.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["IWMPSubscriptionServiceCallback","IWMPSubscriptionServiceCallback interface [Windows Media Player]","IWMPSubscriptionServiceCallback interface [Windows Media Player]","described","IWMPSubscriptionServiceCallbackInterface","subscriptionservices/IWMPSubscriptionServiceCallback","wmp.iwmpsubscriptionservicecallback"]
old-location: wmp\iwmpsubscriptionservicecallback.htm
tech.root: WMP
ms.assetid: c40d492e-030a-4e67-9199-09f44f39a507
ms.date: 4/26/2023
ms.keywords: IWMPSubscriptionServiceCallback, IWMPSubscriptionServiceCallback interface [Windows Media Player], IWMPSubscriptionServiceCallback interface [Windows Media Player],described, IWMPSubscriptionServiceCallbackInterface, subscriptionservices/IWMPSubscriptionServiceCallback, wmp.iwmpsubscriptionservicecallback
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
 - IWMPSubscriptionServiceCallback
 - subscriptionservices/IWMPSubscriptionServiceCallback
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
 - IWMPSubscriptionServiceCallback
---

# IWMPSubscriptionServiceCallback interface


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>IWMPSubscriptionServicesCallback</b> interface defines a method that online stores use to notify Windows Media Player when a background process has completed.

## -inheritance

The <b>IWMPSubscriptionServiceCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPSubscriptionServiceCallback</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/WMP/reference-for-type-2-online-stores">Reference for Type 2 Online Stores</a>
