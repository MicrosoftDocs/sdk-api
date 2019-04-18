---
UID: NF:evcoll.EcRetrySubscription
title: EcRetrySubscription function (evcoll.h)
author: windows-sdk-content
description: Retries connecting to the event source of a subscription that is not connected.
old-location: wec\ecretrysubscription.htm
tech.root: WEC
ms.assetid: 31a9148d-8026-4383-9f31-04b75b4a278d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EcRetrySubscription, EcRetrySubscription function, evcoll/EcRetrySubscription, wec.ecretrysubscription, wes.ecretrysubscription
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
 - EcRetrySubscription
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EcRetrySubscription function


## -description


The <b>EcRetrySubscription</b> function is used to retry connecting to the event source of a subscription that is not connected.


## -parameters




### -param SubscriptionName [in]

The name of the subscription to which to connect.


### -param EventSourceName [in]

The name of the event source of the subscription. This parameter is optional and can be <b>NULL</b>. This parameter must be <b>NULL</b> when the subscription is source initiated.  If this parameter is <b>NULL</b>, the entire subscription will be retried.


### -param Flags [in]

Reserved. Must be <b>NULL</b>.


## -returns



This function returns BOOL.




## -remarks



To retry a subscription for all the event sources of a subscription, use the <a href="https://msdn.microsoft.com/41702fb8-5b39-4daa-8904-aa36de18665c">EcSaveSubscription</a> function instead of calling <b>EcRetrySubscription</b> on each event source individually.


#### Examples

For example code using the <b>EcRetrySubscription</b> function, see <a href="https://msdn.microsoft.com/8a3570af-bde3-40e5-8129-84ec313d853f">Retrying an Event Collector Subscription</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/48155df6-ba9c-4abe-ba84-6190cee95878">Windows Event Collector Functions</a>
 

 

