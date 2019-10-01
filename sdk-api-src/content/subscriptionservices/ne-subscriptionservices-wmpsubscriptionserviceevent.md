---
UID: NE:subscriptionservices.WMPSubscriptionServiceEvent
title: WMPSubscriptionServiceEvent (subscriptionservices.h)
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\wmpsubscriptionserviceevent.htm
tech.root: WMP
ms.assetid: 9d04e534-083b-4227-82aa-4f7e50a492df
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WMPSubscriptionServiceEvent, WMPSubscriptionServiceEvent enumeration [Windows Media Player], enumeration [Windows Media Player], subscriptionservices/WMPSubscriptionServiceEvent, subscriptionservices/wmpsseCurrentBegin, subscriptionservices/wmpsseCurrentEnd, subscriptionservices/wmpsseFullBegin, subscriptionservices/wmpsseFullEnd, wmp.wmpsubscriptionserviceevent, wmpsseCurrentBegin, wmpsseCurrentEnd, wmpsseFullBegin, wmpsseFullEnd
ms.topic: enum
f1_keywords: 
 - "subscriptionservices/WMPSubscriptionServiceEvent"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - subscriptionservices.h
api_name:
 - WMPSubscriptionServiceEvent
targetos: Windows
req.typenames: WMPSubscriptionServiceEvent
req.redist: 
ms.custom: 19H1
---

# WMPSubscriptionServiceEvent enumeration


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>WMPSubscriptionServiceEvent</b> enumeration type defines the types of service events that may occur.




## -enum-fields




### -field wmpsseCurrentBegin

The online store is active.


### -field wmpsseCurrentEnd

The online store is no longer active.


### -field wmpsseFullBegin

The online store is the current active music store.


### -field wmpsseFullEnd

The online store is no longer the current active music store.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/enumerations-for-type-2-online-stores">Enumerations for Type 2 Online Stores</a>
 

 

