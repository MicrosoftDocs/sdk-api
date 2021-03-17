---
UID: NS:mi._MI_SubscriptionDeliveryOptions
title: MI_SubscriptionDeliveryOptions (mi.h)
description: The subscription options object stores configuration options used for passing into subscription operations.
helpviewer_keywords: ["MI_SubscriptionDeliveryOptions","MI_SubscriptionDeliveryOptions structure [Windows Management Infrastructure (MI)]","mi/MI_SubscriptionDeliveryOptions","wmi_v2.mi_subscriptiondeliveryoptions"]
old-location: wmi_v2\mi_subscriptiondeliveryoptions.htm
tech.root: wmi_v2
ms.assetid: aaed635c-ee53-4307-a5b4-e9d3bd2e7c21
ms.date: 12/05/2018
ms.keywords: MI_SubscriptionDeliveryOptions, MI_SubscriptionDeliveryOptions structure [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions, wmi_v2.mi_subscriptiondeliveryoptions
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MI_SubscriptionDeliveryOptions
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_SubscriptionDeliveryOptions
 - mi/_MI_SubscriptionDeliveryOptions
 - MI_SubscriptionDeliveryOptions
 - mi/MI_SubscriptionDeliveryOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_SubscriptionDeliveryOptions
---

# MI_SubscriptionDeliveryOptions structure


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

This structure is created by calling the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newsubscriptiondeliveryoptions">MI_Application_NewSubscriptionDeliveryOptions</a> function.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newsubscriptiondeliveryoptions">MI_Application_NewSubscriptionDeliveryOptions</a>