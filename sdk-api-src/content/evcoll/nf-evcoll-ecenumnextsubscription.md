---
UID: NF:evcoll.EcEnumNextSubscription
title: EcEnumNextSubscription function
author: windows-sdk-content
description: Continues the enumeration of the subscriptions registered on the local machine.
old-location: wec\ecenumnextsubscription.htm
old-project: WEC
ms.assetid: 4228c9ca-6143-4301-8ff3-0ee296a53239
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: EcEnumNextSubscription, EcEnumNextSubscription function, evcoll/EcEnumNextSubscription, wec.ecenumnextsubscription, wes.ecenumnextsubscription
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: evcoll.h
req.include-header: 
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wecapi.dll
api_name:
 - EcEnumNextSubscription
product: Windows
targetos: Windows
req.lib: Wecapi.lib
req.dll: Wecapi.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EcEnumNextSubscription function


## -description


The <b>EcEnumNextSubscription</b> function continues the enumeration of the subscriptions registered on the local machine.


## -parameters




### -param SubscriptionEnum [in]

The handle to the enumerator object that is returned from the <a href="https://msdn.microsoft.com/edbfabb0-6ad1-415a-a2ef-094b1d3bcccb">EcOpenSubscriptionEnum</a> function.


### -param SubscriptionNameBufferSize [in]

The size of the user-supplied buffer (in chars) to store the subscription name.


### -param SubscriptionNameBuffer [in]

The user-supplied buffer to store the subscription name.


### -param SubscriptionNameBufferUsed [out]

The size of the user-supplied buffer that is used by the function on successful return, or the size that is necessary to store the subscription name when the function fails with <b>ERROR_INSUFFICIENT_BUFFER</b>.


## -returns



This function returns BOOL __stdcall.




## -see-also




<a href="https://msdn.microsoft.com/48155df6-ba9c-4abe-ba84-6190cee95878">Windows Event Collector Functions</a>
 

 

