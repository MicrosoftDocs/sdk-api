---
UID: NS:mi._MI_SubscriptionDeliveryOptionsFT
title: MI_SubscriptionDeliveryOptionsFT (mi.h)
description: A support structure used in the MI_SubscriptionDeliveryOptions structure. Use the functions with the name prefix &quot;MI_SubscriptionDeliveryOptions_&quot; to manipulate these structures.
helpviewer_keywords: ["MI_SubscriptionDeliveryOptionsFT","MI_SubscriptionDeliveryOptionsFT structure [Windows Management Infrastructure (MI)]","mi/MI_SubscriptionDeliveryOptionsFT","wmi_v2.mi_subscriptiondeliveryoptionsft"]
old-location: wmi_v2\mi_subscriptiondeliveryoptionsft.htm
tech.root: wmi_v2
ms.assetid: b6f5406a-2abe-4cab-b257-185d77e1fb0e
ms.date: 12/05/2018
ms.keywords: MI_SubscriptionDeliveryOptionsFT, MI_SubscriptionDeliveryOptionsFT structure [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptionsFT, wmi_v2.mi_subscriptiondeliveryoptionsft
f1_keywords:
- mi/MI_SubscriptionDeliveryOptionsFT
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Mi.h
api_name:
- MI_SubscriptionDeliveryOptionsFT
targetos: Windows
req.typenames: MI_SubscriptionDeliveryOptionsFT
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_SubscriptionDeliveryOptionsFT structure


## -description


A support structure used in the <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a> structure.  Use the functions with the name prefix "MI_SubscriptionDeliveryOptions_" to manipulate these structures.


## -struct-fields




### -field MI_Result

TBD 




#### - AddCredentials

Used Internally.


#### - Clone

Creates a copy of a <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a> structure. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_clone">MI_SubscriptionDeliveryOptions_Clone</a>.


#### - Delete

Deletes the specified subscription delivery options structure. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_delete">MI_SubscriptionDeliveryOptions_Delete</a>.


#### - GetCredentialsAt

Gets a previously added credential based on a specified index. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getcredentialsat">MI_SubscriptionDeliveryOptions_GetCredentialsAt</a>.


#### - GetCredentialsCount

Gets the number of previously added credentials. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getcredentialscount">MI_SubscriptionDeliveryOptions_GetCredentialsCount</a>.


#### - GetCredentialsPasswordAt

Gets a previously added credential password based on a specified index. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getcredentialspasswordat">MI_SubscriptionDeliveryOptions_GetCredentialsPasswordAt</a>.


#### - GetDateTime

Gets a previously set DateTime option. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getdatetime">MI_SubscriptionDeliveryOptions_GetDateTime</a>.


#### - GetInterval

Gets the delivery interval for a specified option. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getinterval">MI_SubscriptionDeliveryOptions_GetInterval</a>.


#### - GetNumber

Gets the value of the named numeric option. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getnumber">MI_SubscriptionDeliveryOptions_GetNumber</a>.


#### - GetOption

Gets the value of the named option. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getoption">MI_SubscriptionDeliveryOptions_GetOption</a>.


#### - GetOptionAt

Gets the option at the specified index. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getoptionat">MI_SubscriptionDeliveryOptions_GetOptionAt</a>.


#### - GetOptionCount

Gets the number of previously set options. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getoptioncount">MI_SubscriptionDeliveryOptions_GetOptionCount</a>.


#### - GetString

Gets the value of the named string option. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_getstring">MI_SubscriptionDeliveryOptions_GetString</a>.


#### - SetDateTime

Sets the value of a named DateTime option. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_setdatetime">MI_SubscriptionDeliveryOptions_SetDateTime</a>.


#### - SetInterval

Sets the value of a named interval option. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_setinterval">MI_SubscriptionDeliveryOptions_SetInterval</a>.


#### - SetNumber

Sets the value of a named numeric option. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_setnumber">MI_SubscriptionDeliveryOptions_SetNumber</a>.


#### - SetString

Sets the value of a named string option. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_subscriptiondeliveryoptions_setstring">MI_SubscriptionDeliveryOptions_SetString</a>.

