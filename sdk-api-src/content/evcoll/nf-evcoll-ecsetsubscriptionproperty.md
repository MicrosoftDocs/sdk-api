---
UID: NF:evcoll.EcSetSubscriptionProperty
title: EcSetSubscriptionProperty function
author: windows-sdk-content
description: Sets new values or updates existing values of a subscription.
old-location: wec\ecsetsubscriptionproperty.htm
old-project: WEC
ms.assetid: acba54af-d09d-4de9-bd5d-e7441bf56b9b
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: EcSetSubscriptionProperty, EcSetSubscriptionProperty function, evcoll/EcSetSubscriptionProperty, wec.ecsetsubscriptionproperty, wes.ecsetsubscriptionproperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: EC_VARIANT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wecapi.dll
api_name:
-	EcSetSubscriptionProperty
product: Windows
targetos: Windows
req.lib: Wecapi.lib
req.dll: Wecapi.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EcSetSubscriptionProperty function


## -description


The <b>EcSetSubscriptionProperty</b> function sets new values or updates existing values of a subscription. New values set through this method will not be active unless they are saved by the <a href="https://msdn.microsoft.com/41702fb8-5b39-4daa-8904-aa36de18665c">EcSaveSubscription</a> method.


## -parameters




### -param Subscription [in]

The handle to the subscription object.


### -param PropertyId [in]

A value from the  <a href="https://msdn.microsoft.com/c70dca98-1c14-4c0c-9f2e-6241c463fe4e">EC_SUBSCRIPTION_PROPERTY_ID</a> enumeration that specifies which property of the subscription to set.


### -param Flags [in]

Reserved. Must be 0.


### -param PropertyValue [in]

The value of the property to set for the indicated subscription property.


## -returns



This function returns BOOL.




## -see-also




<a href="https://msdn.microsoft.com/48155df6-ba9c-4abe-ba84-6190cee95878">Windows Event Collector Functions</a>
 

 

