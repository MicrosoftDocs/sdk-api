---
UID: NF:contentpartner.IWMPContentPartner.Notify
title: IWMPContentPartner::Notify (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["IWMPContentPartner interface [Windows Media Player]","Notify method","IWMPContentPartner.Notify","IWMPContentPartner::Notify","IWMPContentPartnerNotify","Notify","Notify method [Windows Media Player]","Notify method [Windows Media Player]","IWMPContentPartner interface","contentpartner/IWMPContentPartner::Notify","wmp.iwmpcontentpartner_notify"]
old-location: wmp\iwmpcontentpartner_notify.htm
tech.root: WMP
ms.assetid: 9464ce82-cd84-4a35-83d2-e46198c0c1e7
ms.date: 12/05/2018
ms.keywords: IWMPContentPartner interface [Windows Media Player],Notify method, IWMPContentPartner.Notify, IWMPContentPartner::Notify, IWMPContentPartnerNotify, Notify, Notify method [Windows Media Player], Notify method [Windows Media Player],IWMPContentPartner interface, contentpartner/IWMPContentPartner::Notify, wmp.iwmpcontentpartner_notify
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
 - IWMPContentPartner::Notify
 - contentpartner/IWMPContentPartner::Notify
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
 - IWMPContentPartner.Notify
---

# IWMPContentPartner::Notify


## -description

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>Notify</b> method provides the content partner plug-in with event notifications from Windows Media Player.

## -parameters

### -param type [in]

The notification type, specified as a member of the <a href="/windows/desktop/api/contentpartner/ne-contentpartner-wmppartnernotification">WMPPartnerNotification</a> enumeration.

### -param pContext [in]

Pointer to a <b>VARIANT</b> that contains notification data.

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

The data type for <i>pContext</i> is <b>VT_EMPTY</b> for all notifications except wmpsnCatalogDownloadFailure. In the case of a catalog download failure, the data type is <b>VT_ERROR</b> and the variable contains an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner">IWMPContentPartner Interface</a>



<a href="/windows/desktop/api/contentpartner/ne-contentpartner-wmppartnernotification">WMPPartnerNotification</a>