---
UID: NF:contentpartner.IWMPContentPartnerCallback.ShowPopup
title: IWMPContentPartnerCallback::ShowPopup (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["IWMPContentPartnerCallback interface [Windows Media Player]","ShowPopup method","IWMPContentPartnerCallback.ShowPopup","IWMPContentPartnerCallback::ShowPopup","IWMPContentPartnerCallbackShowPopup","ShowPopup","ShowPopup method [Windows Media Player]","ShowPopup method [Windows Media Player]","IWMPContentPartnerCallback interface","contentpartner/IWMPContentPartnerCallback::ShowPopup","wmp.iwmpcontentpartnercallback_showpopup"]
old-location: wmp\iwmpcontentpartnercallback_showpopup.htm
tech.root: WMP
ms.assetid: 93b2938c-e3e7-4c9f-92b1-a0b37ed573e6
ms.date: 12/05/2018
ms.keywords: IWMPContentPartnerCallback interface [Windows Media Player],ShowPopup method, IWMPContentPartnerCallback.ShowPopup, IWMPContentPartnerCallback::ShowPopup, IWMPContentPartnerCallbackShowPopup, ShowPopup, ShowPopup method [Windows Media Player], ShowPopup method [Windows Media Player],IWMPContentPartnerCallback interface, contentpartner/IWMPContentPartnerCallback::ShowPopup, wmp.iwmpcontentpartnercallback_showpopup
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
 - IWMPContentPartnerCallback::ShowPopup
 - contentpartner/IWMPContentPartnerCallback::ShowPopup
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
 - IWMPContentPartnerCallback.ShowPopup
---

# IWMPContentPartnerCallback::ShowPopup


## -description

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>ShowPopup</b> method instructs Windows Media Player to display an HTML-based dialog box that hosts a webpage provided by the online store.

## -parameters

### -param lIndex [in]

Index, meaningful only to the online store, of the webpage to display in the dialog box.

### -param bstrParameters [in]

Parameters associated with the dialog box.

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

Windows Media Player calls <a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo">IWMPContentPartner::GetItemInfo</a>, passing the value of <i>lIndex</i> in the <i>pContext</i> parameter, to retrieve a URL. Windows Media Player then appends the value of <i>bstrParameters</i> to the URL, and uses the URL, along with the appended parameters, to retrieve the webpage to display in the dialog box.

You can use the <i>bstrParameters</i> parameter to specify the size of the pop-up window. For example, if you set <i>bstrParameters</i> to "DlgX=800&amp;DlgY=400", the pop-up window will have a size of 800 pixels by 400 pixels.

## -see-also

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback">IWMPContentPartnerCallback Interface</a>