---
UID: NF:evcoll.EcSaveSubscription
title: EcSaveSubscription function
author: windows-sdk-content
description: Saves subscription configuration information.
old-location: wec\ecsavesubscription.htm
tech.root: WEC
ms.assetid: 41702fb8-5b39-4daa-8904-aa36de18665c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EcSaveSubscription, EcSaveSubscription function, evcoll/EcSaveSubscription, wec.ecsavesubscription, wes.ecsavesubscription
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - EcSaveSubscription
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- EcSaveSubscription
: 
---

# EcSaveSubscription function


## -description


The <b>EcSaveSubscription</b> function saves  subscription configuration information. This function should be called whenever new values are added or updated to the subscription by the <a href="https://msdn.microsoft.com/acba54af-d09d-4de9-bd5d-e7441bf56b9b">EcSetSubscriptionProperty</a> method. If the subscription is enabled, the subscription will be activated when it is saved.


## -parameters




### -param Subscription [in]

The handle to the subscription object.


### -param Flags [in]

Reserved. Must be <b>NULL</b>.


## -returns



This function returns BOOL.




## -remarks



To retry a subscription for all the event sources of a subscription, use the <b>EcSaveSubscription</b> function instead of calling <a href="https://msdn.microsoft.com/31a9148d-8026-4383-9f31-04b75b4a278d">EcRetrySubscription</a> on each event source individually.

The subscription will be active only if the collector service is running. The service must be set to automatically start and run after the computer is booted.


#### Examples

For example code using the <b>EcSaveSubscription</b> function, see <a href="https://msdn.microsoft.com/76f14e01-7a84-4c94-aea6-91189573eb89">Creating a Collector Initiated Subscription</a> or <a href="https://msdn.microsoft.com/489d3613-177f-4045-a055-2c1577ef2191">Creating a Source Initiated Subscription</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/48155df6-ba9c-4abe-ba84-6190cee95878">Windows Event Collector Functions</a>
 

 

