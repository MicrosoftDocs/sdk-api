---
UID: NN:subscriptionservices.IWMPSubscriptionServiceCallback
title: IWMPSubscriptionServiceCallback (subscriptionservices.h)
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\iwmpsubscriptionservicecallback.htm
tech.root: WMP
ms.assetid: c40d492e-030a-4e67-9199-09f44f39a507
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPSubscriptionServiceCallback, IWMPSubscriptionServiceCallback interface [Windows Media Player], IWMPSubscriptionServiceCallback interface [Windows Media Player],described, IWMPSubscriptionServiceCallbackInterface, subscriptionservices/IWMPSubscriptionServiceCallback, wmp.iwmpsubscriptionservicecallback
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
 - IWMPSubscriptionServiceCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPSubscriptionServiceCallback interface


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>IWMPSubscriptionServicesCallback</b> interface defines a method that online stores use to notify Windows Media Player when a background process has completed.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPSubscriptionServiceCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPSubscriptionServiceCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPSubscriptionServiceCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563704(v=VS.85).aspx">onComplete</a>
</td>
<td align="left" width="63%">
Notifies the Player when a background process is completed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b3f580cc-b02d-4312-a7a1-a35778a222bc">Reference for Type 2 Online Stores</a>
 

 

