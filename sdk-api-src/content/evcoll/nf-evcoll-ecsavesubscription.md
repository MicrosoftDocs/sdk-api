---
UID: NF:evcoll.EcSaveSubscription
title: EcSaveSubscription function (evcoll.h)
description: Saves subscription configuration information.
helpviewer_keywords: ["EcSaveSubscription","EcSaveSubscription function","evcoll/EcSaveSubscription","wec.ecsavesubscription","wes.ecsavesubscription"]
old-location: wec\ecsavesubscription.htm
tech.root: WEC
ms.assetid: 41702fb8-5b39-4daa-8904-aa36de18665c
ms.date: 12/05/2018
ms.keywords: EcSaveSubscription, EcSaveSubscription function, evcoll/EcSaveSubscription, wec.ecsavesubscription, wes.ecsavesubscription
req.header: evcoll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wecapi.lib
req.dll: Wecapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EcSaveSubscription
 - evcoll/EcSaveSubscription
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wecapi.dll
api_name:
 - EcSaveSubscription
---

# EcSaveSubscription function


## -description

The <b>EcSaveSubscription</b> function saves  subscription configuration information. This function should be called whenever new values are added or updated to the subscription by the <a href="/windows/desktop/api/evcoll/nf-evcoll-ecsetsubscriptionproperty">EcSetSubscriptionProperty</a> method. If the subscription is enabled, the subscription will be activated when it is saved.

## -parameters

### -param Subscription [in]

The handle to the subscription object.

### -param Flags [in]

Reserved. Must be <b>NULL</b>.

## -returns

This function returns BOOL.

## -remarks

To retry a subscription for all the event sources of a subscription, use the <b>EcSaveSubscription</b> function instead of calling <a href="/windows/desktop/api/evcoll/nf-evcoll-ecretrysubscription">EcRetrySubscription</a> on each event source individually.

The subscription will be active only if the collector service is running. The service must be set to automatically start and run after the computer is booted.


#### Examples

For example code using the <b>EcSaveSubscription</b> function, see <a href="/windows/desktop/WEC/creating-an-event-collector-subscription">Creating a Collector Initiated Subscription</a> or <a href="/windows/desktop/WEC/creating-a-source-initiated-subscription">Creating a Source Initiated Subscription</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/WEC/windows-event-collector-functions">Windows Event Collector Functions</a>