---
UID: NF:subscriptionservices.IWMPSubscriptionService2.stopBackgroundProcessing
title: IWMPSubscriptionService2::stopBackgroundProcessing (subscriptionservices.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["IWMPSubscriptionService2 interface [Windows Media Player]","stopBackgroundProcessing method","IWMPSubscriptionService2.stopBackgroundProcessing","IWMPSubscriptionService2::stopBackgroundProcessing","IWMPSubscriptionService2stopBackgroundProcessing","stopBackgroundProcessing","stopBackgroundProcessing method [Windows Media Player]","stopBackgroundProcessing method [Windows Media Player]","IWMPSubscriptionService2 interface","subscriptionservices/IWMPSubscriptionService2::stopBackgroundProcessing","wmp.iwmpsubscriptionservice2_stopbackgroundprocessing"]
old-location: wmp\iwmpsubscriptionservice2_stopbackgroundprocessing.htm
tech.root: WMP
ms.assetid: afca5ab8-d7ca-48e9-8220-d132d1893f0e
ms.date: 12/05/2018
ms.keywords: IWMPSubscriptionService2 interface [Windows Media Player],stopBackgroundProcessing method, IWMPSubscriptionService2.stopBackgroundProcessing, IWMPSubscriptionService2::stopBackgroundProcessing, IWMPSubscriptionService2stopBackgroundProcessing, stopBackgroundProcessing, stopBackgroundProcessing method [Windows Media Player], stopBackgroundProcessing method [Windows Media Player],IWMPSubscriptionService2 interface, subscriptionservices/IWMPSubscriptionService2::stopBackgroundProcessing, wmp.iwmpsubscriptionservice2_stopbackgroundprocessing
req.header: subscriptionservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 10 or later.
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
 - IWMPSubscriptionService2::stopBackgroundProcessing
 - subscriptionservices/IWMPSubscriptionService2::stopBackgroundProcessing
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
 - IWMPSubscriptionService2.stopBackgroundProcessing
---

# IWMPSubscriptionService2::stopBackgroundProcessing


## -description

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>stopBackgroundProcessing</b> method is implemented by the online store to terminate background processing tasks.



## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

Calls to <b>stopBackgroundProcessing</b> occur after calls to <b>startBackgroundProcessing</b> to signal the online store that background processing tasks must be suspended.

## -see-also

<a href="/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2">IWMPSubscriptionService2 Interface</a>
