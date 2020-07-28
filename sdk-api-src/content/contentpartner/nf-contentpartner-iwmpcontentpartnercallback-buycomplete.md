---
UID: NF:contentpartner.IWMPContentPartnerCallback.BuyComplete
title: IWMPContentPartnerCallback::BuyComplete (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["BuyComplete","BuyComplete method [Windows Media Player]","BuyComplete method [Windows Media Player]","IWMPContentPartnerCallback interface","IWMPContentPartnerCallback interface [Windows Media Player]","BuyComplete method","IWMPContentPartnerCallback.BuyComplete","IWMPContentPartnerCallback::BuyComplete","IWMPContentPartnerCallbackBuyComplete","contentpartner/IWMPContentPartnerCallback::BuyComplete","wmp.iwmpcontentpartnercallback_buycomplete"]
old-location: wmp\iwmpcontentpartnercallback_buycomplete.htm
tech.root: WMP
ms.assetid: 4e9ab15f-3418-472d-afc4-0f9fae852da2
ms.date: 12/05/2018
ms.keywords: BuyComplete, BuyComplete method [Windows Media Player], BuyComplete method [Windows Media Player],IWMPContentPartnerCallback interface, IWMPContentPartnerCallback interface [Windows Media Player],BuyComplete method, IWMPContentPartnerCallback.BuyComplete, IWMPContentPartnerCallback::BuyComplete, IWMPContentPartnerCallbackBuyComplete, contentpartner/IWMPContentPartnerCallback::BuyComplete, wmp.iwmpcontentpartnercallback_buycomplete
f1_keywords:
- contentpartner/IWMPContentPartnerCallback.BuyComplete
dev_langs:
- c++
req.header: contentpartner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11
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
- contentpartner.h
api_name:
- IWMPContentPartnerCallback.BuyComplete
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPContentPartnerCallback::BuyComplete


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>BuyComplete</b> method notifies Windows Media Player that a purchase transaction has been completed.




## -parameters




### -param hrResult [in]

<b>HRESULT</b> return code indicating the success or failure of the transaction.


### -param dwBuyCookie [in]

The cookie that represents the purchase transaction. This value was provided when the Player called <a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy">IWMPContentPartner::Buy</a>.


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



You must call <b>BuyComplete</b> exactly once for each call to <a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy">IWMPContentPartner::Buy</a>. Call <b>BuyComplete</b> when the transaction is finished, even if it failed for some reason.

Return a success code only after all licenses related to the purchase have been delivered.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback">IWMPContentPartnerCallback Interface</a>
 

 

