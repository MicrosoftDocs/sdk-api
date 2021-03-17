---
UID: NF:mi.MI_SubscriptionDeliveryOptions_AddDeliveryCredentials
title: MI_SubscriptionDeliveryOptions_AddDeliveryCredentials function (mi.h)
description: Sets a subscription option for delivery credentials to use when connecting back to the client to deliver a push indication result.
helpviewer_keywords: ["MI_SubscriptionDeliveryOptions_AddDeliveryCredentials","MI_SubscriptionDeliveryOptions_AddDeliveryCredentials function [Windows Management Infrastructure (MI)]","mi/MI_SubscriptionDeliveryOptions_AddDeliveryCredentials","wmi_v2.mi_subscriptiondeliveryoptions_adddeliverycredentials"]
old-location: wmi_v2\mi_subscriptiondeliveryoptions_adddeliverycredentials.htm
tech.root: wmi_v2
ms.assetid: ce531ffb-adaa-49df-a051-da51e04196b3
ms.date: 12/05/2018
ms.keywords: MI_SubscriptionDeliveryOptions_AddDeliveryCredentials, MI_SubscriptionDeliveryOptions_AddDeliveryCredentials function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_AddDeliveryCredentials, wmi_v2.mi_subscriptiondeliveryoptions_adddeliverycredentials
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
 - MI_SubscriptionDeliveryOptions_AddDeliveryCredentials
 - mi/MI_SubscriptionDeliveryOptions_AddDeliveryCredentials
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
 - MI_SubscriptionDeliveryOptions_AddDeliveryCredentials
---

# MI_SubscriptionDeliveryOptions_AddDeliveryCredentials function


## -description

Sets a subscription option for delivery credentials to use when connecting back to the client to deliver a push indication result.

## -parameters

### -param self [in, out]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a> structure.

### -param value [in]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_usercredentials">MI_UserCredentials</a> structure.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

This setting is only used by <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a> (WinRM). The currently supported authentication modes are IssuerCert and Kerberos.