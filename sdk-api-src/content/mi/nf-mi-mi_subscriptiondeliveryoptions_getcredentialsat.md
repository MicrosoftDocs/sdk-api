---
UID: NF:mi.MI_SubscriptionDeliveryOptions_GetCredentialsAt
title: MI_SubscriptionDeliveryOptions_GetCredentialsAt function (mi.h)
description: Gets a previously added credential based on a specified index.
helpviewer_keywords: ["MI_SubscriptionDeliveryOptions_GetCredentialsAt","MI_SubscriptionDeliveryOptions_GetCredentialsAt function [Windows Management Infrastructure (MI)]","mi/MI_SubscriptionDeliveryOptions_GetCredentialsAt","wmi_v2.mi_subscriptiondeliveryoptions_getcredentialsat"]
old-location: wmi_v2\mi_subscriptiondeliveryoptions_getcredentialsat.htm
tech.root: wmi_v2
ms.assetid: 3af2ec8f-27fa-4adf-9946-07a1dcb0d0e8
ms.date: 12/05/2018
ms.keywords: MI_SubscriptionDeliveryOptions_GetCredentialsAt, MI_SubscriptionDeliveryOptions_GetCredentialsAt function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_GetCredentialsAt, wmi_v2.mi_subscriptiondeliveryoptions_getcredentialsat
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
 - MI_SubscriptionDeliveryOptions_GetCredentialsAt
 - mi/MI_SubscriptionDeliveryOptions_GetCredentialsAt
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
 - MI_SubscriptionDeliveryOptions_GetCredentialsAt
---

# MI_SubscriptionDeliveryOptions_GetCredentialsAt function


## -description

Gets a previously added credential based on a specified index.

## -parameters

### -param self [in]

A <a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a> structure.

### -param index

Zero-based index of the credential.

### -param optionName

A pointer to a null-terminated string containing the returned credential name.

### -param credentials [out]

Returned user credentials. Passwords are always set to asterisks for security reasons. To get the actual password, call the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getcredentialspasswordat">MI_SubscriptionDeliveryOptions_GetCredentialsPasswordAt</a> function.

### -param flags [out, optional]

Returned credential flags.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -see-also

<a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getcredentialspasswordat">MI_SubscriptionDeliveryOptions_GetCredentialsPasswordAt</a>