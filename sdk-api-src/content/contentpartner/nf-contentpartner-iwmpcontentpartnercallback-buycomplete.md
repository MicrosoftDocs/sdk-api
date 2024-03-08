---
UID: NF:contentpartner.IWMPContentPartnerCallback.BuyComplete
title: IWMPContentPartnerCallback::BuyComplete (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["BuyComplete","BuyComplete method [Windows Media Player]","BuyComplete method [Windows Media Player]","IWMPContentPartnerCallback interface","IWMPContentPartnerCallback interface [Windows Media Player]","BuyComplete method","IWMPContentPartnerCallback.BuyComplete","IWMPContentPartnerCallback::BuyComplete","IWMPContentPartnerCallbackBuyComplete","contentpartner/IWMPContentPartnerCallback::BuyComplete","wmp.iwmpcontentpartnercallback_buycomplete"]
old-location: wmp\iwmpcontentpartnercallback_buycomplete.htm
tech.root: WMP
ms.assetid: 4e9ab15f-3418-472d-afc4-0f9fae852da2
ms.date: 4/26/2023
ms.keywords: BuyComplete, BuyComplete method [Windows Media Player], BuyComplete method [Windows Media Player],IWMPContentPartnerCallback interface, IWMPContentPartnerCallback interface [Windows Media Player],BuyComplete method, IWMPContentPartnerCallback.BuyComplete, IWMPContentPartnerCallback::BuyComplete, IWMPContentPartnerCallbackBuyComplete, contentpartner/IWMPContentPartnerCallback::BuyComplete, wmp.iwmpcontentpartnercallback_buycomplete
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPContentPartnerCallback::BuyComplete
 - contentpartner/IWMPContentPartnerCallback::BuyComplete
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - contentpartner.h
api_name:
 - IWMPContentPartnerCallback.BuyComplete
---

# IWMPContentPartnerCallback::BuyComplete


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>BuyComplete</b> method notifies Windows Media Player that a purchase transaction has been completed.

## -parameters

### -param hrResult [in]

<b>HRESULT</b> return code indicating the success or failure of the transaction.

### -param dwBuyCookie [in]

The cookie that represents the purchase transaction. This value was provided when the Player called <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy">IWMPContentPartner::Buy</a>.

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

You must call <b>BuyComplete</b> exactly once for each call to <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy">IWMPContentPartner::Buy</a>. Call <b>BuyComplete</b> when the transaction is finished, even if it failed for some reason.

Return a success code only after all licenses related to the purchase have been delivered.

## -see-also

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback">IWMPContentPartnerCallback Interface</a>