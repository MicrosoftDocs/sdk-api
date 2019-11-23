---
UID: NE:contentpartner.WMPPartnerNotification
title: WMPPartnerNotification (contentpartner.h)

description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The WMPPartnerNotification enumeration defines operational states of an online store.
old-location: wmp\wmppartnernotification.htm
tech.root: WMP
ms.assetid: a9292277-5283-41b8-86a6-f7059aa38a69

ms.date: 12/05/2018
ms.keywords: WMPPartnerNotification, WMPPartnerNotification enumeration [Windows Media Player], contentpartner/WMPPartnerNotification, contentpartner/wmpsnBackgroundProcessingBegin, contentpartner/wmpsnBackgroundProcessingEnd, contentpartner/wmpsnCatalogDownloadComplete, contentpartner/wmpsnCatalogDownloadFailure, enumeration [Windows Media Player], wmp.wmppartnernotification, wmpsnBackgroundProcessingBegin, wmpsnBackgroundProcessingEnd, wmpsnCatalogDownloadComplete, wmpsnCatalogDownloadFailure
ms.topic: enum
f1_keywords: 
 - "contentpartner/WMPPartnerNotification"
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
 - HeaderDef
api_location:
 - contentpartner.h
api_name:
 - WMPPartnerNotification
targetos: Windows
req.typenames: WMPPartnerNotification
req.redist: 
ms.custom: 19H1
---

# WMPPartnerNotification enumeration


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>WMPPartnerNotification</b> enumeration defines operational states of an online store.




## -enum-fields




### -field wmpsnBackgroundProcessingBegin

Start background processing.


### -field wmpsnBackgroundProcessingEnd

End background processing.


### -field wmpsnCatalogDownloadFailure

The catalog download failed.


### -field wmpsnCatalogDownloadComplete

The catalog download completed.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/enumerations-for-type-1-online-stores">Enumerations for Type 1 Online Stores</a>



<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify">IWMPContentPartner::Notify</a>
 

 

