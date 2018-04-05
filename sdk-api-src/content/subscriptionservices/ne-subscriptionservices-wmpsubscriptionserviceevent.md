---
UID: NE:subscriptionservices.WMPSubscriptionServiceEvent
title: WMPSubscriptionServiceEvent
author: windows-driver-content
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\wmpsubscriptionserviceevent.htm
old-project: WMP
ms.assetid: 9d04e534-083b-4227-82aa-4f7e50a492df
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: WMPSubscriptionServiceEvent, WMPSubscriptionServiceEvent enumeration [Windows Media Player], enumeration [Windows Media Player], subscriptionservices/WMPSubscriptionServiceEvent, subscriptionservices/wmpsseCurrentBegin, subscriptionservices/wmpsseCurrentEnd, subscriptionservices/wmpsseFullBegin, subscriptionservices/wmpsseFullEnd, wmp.wmpsubscriptionserviceevent, wmpsseCurrentBegin, wmpsseCurrentEnd, wmpsseFullBegin, wmpsseFullEnd
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: WMPSubscriptionServiceEvent
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	subscriptionservices.h
api_name:
-	WMPSubscriptionServiceEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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




<a href="https://msdn.microsoft.com/b4d27310-9902-4c46-a558-f46f19735ec7">Enumerations for Type 2 Online Stores</a>
 

 

