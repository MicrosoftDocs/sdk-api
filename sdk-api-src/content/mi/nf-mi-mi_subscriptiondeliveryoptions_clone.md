---
UID: NF:mi.MI_SubscriptionDeliveryOptions_Clone
title: MI_SubscriptionDeliveryOptions_Clone function (mi.h)
description: Creates a copy of a MI_SubscriptionDeliveryOptions structure.
helpviewer_keywords: ["MI_SubscriptionDeliveryOptions_Clone","MI_SubscriptionDeliveryOptions_Clone function [Windows Management Infrastructure (MI)]","mi/MI_SubscriptionDeliveryOptions_Clone","wmi_v2.mi_subscriptiondeliveryoptions_clone"]
old-location: wmi_v2\mi_subscriptiondeliveryoptions_clone.htm
tech.root: wmi_v2
ms.assetid: 34374907-bbb6-4d22-81ac-2d662efaf119
ms.date: 12/05/2018
ms.keywords: MI_SubscriptionDeliveryOptions_Clone, MI_SubscriptionDeliveryOptions_Clone function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_Clone, wmi_v2.mi_subscriptiondeliveryoptions_clone
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
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_SubscriptionDeliveryOptions_Clone
 - mi/MI_SubscriptionDeliveryOptions_Clone
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
 - MI_SubscriptionDeliveryOptions_Clone
---

# MI_SubscriptionDeliveryOptions_Clone function


## -description

Creates a copy of a <a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a> structure.

## -parameters

### -param self [in]

<a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a> structure to be cloned.

### -param newSubscriptionDeliveryOptions [out]

Returned <a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a> clone. This clone will eventually need to be deleted by calling the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_delete">MI_SubscriptionDeliveryOptions_Delete</a> function.

## -returns

This function returns MI_INLINE MI_Result MI_INLINE_CALL.

## -see-also

<a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_delete">MI_SubscriptionDeliveryOptions_Delete</a>