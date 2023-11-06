---
UID: NF:contentpartner.IWMPContentPartner.Buy
title: IWMPContentPartner::Buy (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The Buy method initiates the purchase of digital media content.
helpviewer_keywords: ["Buy","Buy method [Windows Media Player]","Buy method [Windows Media Player]","IWMPContentPartner interface","IWMPContentPartner interface [Windows Media Player]","Buy method","IWMPContentPartner.Buy","IWMPContentPartner::Buy","IWMPContentPartnerBuy","contentpartner/IWMPContentPartner::Buy","wmp.iwmpcontentpartner_buy"]
old-location: wmp\iwmpcontentpartner_buy.htm
tech.root: WMP
ms.assetid: a79c3d6e-b587-4bbc-b3bf-6489a54d71f9
ms.date: 4/26/2023
ms.keywords: Buy, Buy method [Windows Media Player], Buy method [Windows Media Player],IWMPContentPartner interface, IWMPContentPartner interface [Windows Media Player],Buy method, IWMPContentPartner.Buy, IWMPContentPartner::Buy, IWMPContentPartnerBuy, contentpartner/IWMPContentPartner::Buy, wmp.iwmpcontentpartner_buy
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
 - IWMPContentPartner::Buy
 - contentpartner/IWMPContentPartner::Buy
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
 - IWMPContentPartner.Buy
---

# IWMPContentPartner::Buy


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>Buy</b> method initiates the purchase of digital media content.

## -parameters

### -param pInfo [in]

Pointer to a content container list that represents the content to be purchased.

### -param cookie [in]

A cookie used to identify the transaction. You must store this value and pass it to <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-buycomplete">IWMPContentPartnerCallback::BuyComplete</a> when the purchase transaction is finished.

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

You must call <b>IWMPContentPartnerCallback::BuyComplete</b> exactly once for each call to <b>Buy</b>. Call <b>BuyComplete</b> when the transaction is finished, even if it failed for some reason.

If the user has an expired license for content previously purchased, you can simply update the license.

## -see-also

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner">IWMPContentPartner Interface</a>