---
UID: NE:contentpartner.WMPAccountType
title: WMPAccountType (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The WMPAccountType enumeration defines account types for an online store.
helpviewer_keywords: ["WMPAccountType","WMPAccountType enumeration [Windows Media Player]","contentpartner/WMPAccountType","contentpartner/wmpatBuyOnly","contentpartner/wmpatJanus","contentpartner/wmpatSubscription","enumeration [Windows Media Player]","wmp.wmpaccounttype","wmpatBuyOnly","wmpatJanus","wmpatSubscription"]
old-location: wmp\wmpaccounttype.htm
tech.root: WMP
ms.assetid: daab6937-0906-4b69-8d00-c68e43b8214f
ms.date: 12/05/2018
ms.keywords: WMPAccountType, WMPAccountType enumeration [Windows Media Player], contentpartner/WMPAccountType, contentpartner/wmpatBuyOnly, contentpartner/wmpatJanus, contentpartner/wmpatSubscription, enumeration [Windows Media Player], wmp.wmpaccounttype, wmpatBuyOnly, wmpatJanus, wmpatSubscription
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
req.typenames: WMPAccountType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMPAccountType
 - contentpartner/WMPAccountType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - contentpartner.h
api_name:
 - WMPAccountType
---

# WMPAccountType enumeration


## -description

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>WMPAccountType</b> enumeration defines account types for an online store.

## -enum-fields

### -field wmpatBuyOnly:1

The user is only authorized to purchase content.

### -field wmpatSubscription:2

The user has a subscription account, but content must be purchased to synchronize to a device based on Windows Media DRM for Portable Devices.

### -field wmpatJanus:3

The user has a subscription account and the subscription content can be synchronized to a device based on Windows Media DRM for Portable Devices.

## -see-also

<a href="/windows/desktop/WMP/enumerations-for-type-1-online-stores">Enumerations for Type 1 Online Stores</a>



<a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo">IWMPContentPartner::GetContentPartnerInfo</a>
