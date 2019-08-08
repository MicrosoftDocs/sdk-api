---
UID: NF:evcoll.EcSetSubscriptionProperty
title: EcSetSubscriptionProperty function (evcoll.h)
author: windows-sdk-content
description: Sets new values or updates existing values of a subscription.
old-location: wec\ecsetsubscriptionproperty.htm
tech.root: WEC
ms.assetid: acba54af-d09d-4de9-bd5d-e7441bf56b9b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EcSetSubscriptionProperty, EcSetSubscriptionProperty function, evcoll/EcSetSubscriptionProperty, wec.ecsetsubscriptionproperty, wes.ecsetsubscriptionproperty
ms.topic: function
f1_keywords:
- evcoll/EcSetSubscriptionProperty
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Wecapi.dll
api_name:
- EcSetSubscriptionProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EcSetSubscriptionProperty function


## -description


The <b>EcSetSubscriptionProperty</b> function sets new values or updates existing values of a subscription. New values set through this method will not be active unless they are saved by the <a href="https://docs.microsoft.com/windows/desktop/api/evcoll/nf-evcoll-ecsavesubscription">EcSaveSubscription</a> method.


## -parameters




### -param Subscription [in]

The handle to the subscription object.


### -param PropertyId [in]

A value from the  <a href="https://docs.microsoft.com/windows/desktop/api/evcoll/ne-evcoll-ec_subscription_property_id">EC_SUBSCRIPTION_PROPERTY_ID</a> enumeration that specifies which property of the subscription to set.


### -param Flags [in]

Reserved. Must be 0.


### -param PropertyValue [in]

The value of the property to set for the indicated subscription property.


## -returns



This function returns BOOL.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WEC/windows-event-collector-functions">Windows Event Collector Functions</a>
 

 

