---
UID: NF:eventsys.IEventSubscription.get_Enabled
title: IEventSubscription::get_Enabled (eventsys.h)
description: Indicates whether the subscription is enabled. (Get)
helpviewer_keywords: ["Enabled property [COM+]","Enabled property [COM+]","IEventSubscription interface","IEventSubscription interface [COM+]","Enabled property","IEventSubscription.Enabled","IEventSubscription.get_Enabled","IEventSubscription::Enabled","IEventSubscription::get_Enabled","IEventSubscription::put_Enabled","cos.ieventsubscription_enabled","eventsys/IEventSubscription::Enabled","eventsys/IEventSubscription::get_Enabled","eventsys/IEventSubscription::put_Enabled","get_Enabled"]
old-location: cos\ieventsubscription_enabled.htm
tech.root: cos
ms.assetid: 02481b3d-1064-448f-955b-0dd02d90db46
ms.date: 12/05/2018
ms.keywords: Enabled property [COM+], Enabled property [COM+],IEventSubscription interface, IEventSubscription interface [COM+],Enabled property, IEventSubscription.Enabled, IEventSubscription.get_Enabled, IEventSubscription::Enabled, IEventSubscription::get_Enabled, IEventSubscription::put_Enabled, cos.ieventsubscription_enabled, eventsys/IEventSubscription::Enabled, eventsys/IEventSubscription::get_Enabled, eventsys/IEventSubscription::put_Enabled, get_Enabled
req.header: eventsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: EventSys.idl
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
 - IEventSubscription::get_Enabled
 - eventsys/IEventSubscription::get_Enabled
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EventSys.h
api_name:
 - IEventSubscription.Enabled
 - IEventSubscription.get_Enabled
 - IEventSubscription.put_Enabled
---

# IEventSubscription::get_Enabled


## -description

Indicates whether the subscription is enabled.

This property is read/write.

## -parameters

## -remarks

If a subscription is not enabled, it still appears in collections and can be queried, but events fired by the publisher do not reach the subscriber.

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventsubscription">IEventSubscription</a>
