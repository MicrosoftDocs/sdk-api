---
UID: NS:mi._MI_SubscriptionDeliveryOptions
title: "_MI_SubscriptionDeliveryOptions"
author: windows-driver-content
description: The subscription options object stores configuration options used for passing into subscription operations.
old-location: wmi_v2\mi_subscriptiondeliveryoptions.htm
old-project: wmi_v2
ms.assetid: aaed635c-ee53-4307-a5b4-e9d3bd2e7c21
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: MI_SubscriptionDeliveryOptions, MI_SubscriptionDeliveryOptions structure [Windows Management Infrastructure (MI)], _MI_SubscriptionDeliveryOptions, mi/MI_SubscriptionDeliveryOptions, wmi_v2.mi_subscriptiondeliveryoptions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MI_SubscriptionDeliveryOptions, MI_SubscriptionDeliveryOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_SubscriptionDeliveryOptions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MI_SubscriptionDeliveryOptions structure


## -description


The subscription options object stores configuration options used for passing into subscription operations.


## -struct-fields




### -field reserved1

Reserved for internal use only.


### -field reserved2

Reserved for internal use only.


### -field ft

Pointer to the <b>MI_SubscriptionDeliveryOptions</b> function table.


## -remarks



This structure is created by calling the <a href="https://msdn.microsoft.com/ac84ec09-7d91-42fc-8271-3e0e54bbb788">MI_Application_NewSubscriptionDeliveryOptions</a> function.




## -see-also




<a href="https://msdn.microsoft.com/ac84ec09-7d91-42fc-8271-3e0e54bbb788">MI_Application_NewSubscriptionDeliveryOptions</a>
 

 

