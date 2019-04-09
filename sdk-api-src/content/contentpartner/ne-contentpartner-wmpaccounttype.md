---
UID: NE:contentpartner.WMPAccountType
title: WMPAccountType (contentpartner.h)
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The WMPAccountType enumeration defines account types for an online store.
old-location: wmp\wmpaccounttype.htm
tech.root: WMP
ms.assetid: daab6937-0906-4b69-8d00-c68e43b8214f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WMPAccountType, WMPAccountType enumeration [Windows Media Player], contentpartner/WMPAccountType, contentpartner/wmpatBuyOnly, contentpartner/wmpatJanus, contentpartner/wmpatSubscription, enumeration [Windows Media Player], wmp.wmpaccounttype, wmpatBuyOnly, wmpatJanus, wmpatSubscription
ms.topic: enum
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
 - HeaderDef
api_location:
 - contentpartner.h
api_name:
 - WMPAccountType
product: Windows
targetos: Windows
req.typenames: WMPAccountType
req.redist: 
---

# WMPAccountType enumeration


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>WMPAccountType</b> enumeration defines account types for an online store.




## -enum-fields




### -field wmpatBuyOnly

The user is only authorized to purchase content.


### -field wmpatSubscription

The user has a subscription account, but content must be purchased to synchronize to a device based on Windows Media DRM for Portable Devices.


### -field wmpatJanus

The user has a subscription account and the subscription content can be synchronized to a device based on Windows Media DRM for Portable Devices.


## -see-also




<a href="https://msdn.microsoft.com/7359585f-6e8f-498f-a5a2-230265bae147">Enumerations for Type 1 Online Stores</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563164(v=VS.85).aspx">IWMPContentPartner::GetContentPartnerInfo</a>
 

 

