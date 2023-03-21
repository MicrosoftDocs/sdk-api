---
UID: NE:subscriptionservices.WMPSubscriptionServiceEvent
title: WMPSubscriptionServiceEvent (subscriptionservices.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["WMPSubscriptionServiceEvent","WMPSubscriptionServiceEvent enumeration [Windows Media Player]","enumeration [Windows Media Player]","subscriptionservices/WMPSubscriptionServiceEvent","subscriptionservices/wmpsseCurrentBegin","subscriptionservices/wmpsseCurrentEnd","subscriptionservices/wmpsseFullBegin","subscriptionservices/wmpsseFullEnd","wmp.wmpsubscriptionserviceevent","wmpsseCurrentBegin","wmpsseCurrentEnd","wmpsseFullBegin","wmpsseFullEnd"]
old-location: wmp\wmpsubscriptionserviceevent.htm
tech.root: WMP
ms.assetid: 9d04e534-083b-4227-82aa-4f7e50a492df
ms.date: 12/05/2018
ms.keywords: WMPSubscriptionServiceEvent, WMPSubscriptionServiceEvent enumeration [Windows Media Player], enumeration [Windows Media Player], subscriptionservices/WMPSubscriptionServiceEvent, subscriptionservices/wmpsseCurrentBegin, subscriptionservices/wmpsseCurrentEnd, subscriptionservices/wmpsseFullBegin, subscriptionservices/wmpsseFullEnd, wmp.wmpsubscriptionserviceevent, wmpsseCurrentBegin, wmpsseCurrentEnd, wmpsseFullBegin, wmpsseFullEnd
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
targetos: Windows
req.typenames: WMPSubscriptionServiceEvent
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMPSubscriptionServiceEvent
 - subscriptionservices/WMPSubscriptionServiceEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - subscriptionservices.h
api_name:
 - WMPSubscriptionServiceEvent
---

# WMPSubscriptionServiceEvent enumeration


## -description

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>WMPSubscriptionServiceEvent</b> enumeration type defines the types of service events that may occur.

## -enum-fields

### -field wmpsseCurrentBegin:1

The online store is active.

### -field wmpsseCurrentEnd:2

The online store is no longer active.

### -field wmpsseFullBegin:3

The online store is the current active music store.

### -field wmpsseFullEnd:4

The online store is no longer the current active music store.

## -see-also

<a href="/windows/desktop/WMP/enumerations-for-type-2-online-stores">Enumerations for Type 2 Online Stores</a>
