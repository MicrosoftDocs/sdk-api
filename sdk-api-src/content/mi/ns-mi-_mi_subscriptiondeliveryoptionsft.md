---
UID: NS:mi._MI_SubscriptionDeliveryOptionsFT
title: "_MI_SubscriptionDeliveryOptionsFT"
author: windows-sdk-content
description: A support structure used in the MI_SubscriptionDeliveryOptions structure. Use the functions with the name prefix &#0034;MI_SubscriptionDeliveryOptions_&#0034; to manipulate these structures.
old-location: wmi_v2\mi_subscriptiondeliveryoptionsft.htm
old-project: wmi_v2
ms.assetid: b6f5406a-2abe-4cab-b257-185d77e1fb0e
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: MI_SubscriptionDeliveryOptionsFT, MI_SubscriptionDeliveryOptionsFT structure [Windows Management Infrastructure (MI)], _MI_SubscriptionDeliveryOptionsFT, mi/MI_SubscriptionDeliveryOptionsFT, wmi_v2.mi_subscriptiondeliveryoptionsft
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MI_SubscriptionDeliveryOptionsFT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_SubscriptionDeliveryOptionsFT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MI_SubscriptionDeliveryOptionsFT structure


## -description


A support structure used in the <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> structure.  Use the functions with the name prefix "MI_SubscriptionDeliveryOptions_" to manipulate these structures.


## -struct-fields






#### - AddCredentials

Used Internally.


#### - Clone

Creates a copy of a <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> structure. See <a href="https://msdn.microsoft.com/34374907-bbb6-4d22-81ac-2d662efaf119">MI_SubscriptionDeliveryOptions_Clone</a>.


#### - Delete

Deletes the specified subscription delivery options structure. See <a href="https://msdn.microsoft.com/658dcb26-4ba1-42ef-a404-b431d0c92864">MI_SubscriptionDeliveryOptions_Delete</a>.


#### - GetCredentialsAt

Gets a previously added credential based on a specified index. See <a href="https://msdn.microsoft.com/3af2ec8f-27fa-4adf-9946-07a1dcb0d0e8">MI_SubscriptionDeliveryOptions_GetCredentialsAt</a>.


#### - GetCredentialsCount

Gets the number of previously added credentials. See <a href="https://msdn.microsoft.com/6d9286ac-70e0-4290-8cbf-11514510dcdb">MI_SubscriptionDeliveryOptions_GetCredentialsCount</a>.


#### - GetCredentialsPasswordAt

Gets a previously added credential password based on a specified index. See <a href="https://msdn.microsoft.com/338fba5a-160e-4744-84c5-28aa1f115f53">MI_SubscriptionDeliveryOptions_GetCredentialsPasswordAt</a>.


#### - GetDateTime

Gets a previously set DateTime option. See <a href="https://msdn.microsoft.com/502738a3-1f4a-460c-bd1c-5f1ea411d899">MI_SubscriptionDeliveryOptions_GetDateTime</a>.


#### - GetInterval

Gets the delivery interval for a specified option. See <a href="https://msdn.microsoft.com/f515bfbf-2f28-4ee0-8f60-8725206b3568">MI_SubscriptionDeliveryOptions_GetInterval</a>.


#### - GetNumber

Gets the value of the named numeric option. See <a href="https://msdn.microsoft.com/80314490-204d-4b99-937f-f9b55266ac1a">MI_SubscriptionDeliveryOptions_GetNumber</a>.


#### - GetOption

Gets the value of the named option. See <a href="https://msdn.microsoft.com/4245b569-afe4-46e0-8d32-e7b571104071">MI_SubscriptionDeliveryOptions_GetOption</a>.


#### - GetOptionAt

Gets the option at the specified index. See <a href="https://msdn.microsoft.com/7ee9fc4a-b836-4820-84b6-925d9842819d">MI_SubscriptionDeliveryOptions_GetOptionAt</a>.


#### - GetOptionCount

Gets the number of previously set options. See <a href="https://msdn.microsoft.com/695a4ec8-4e6b-4a3d-800b-fa0edfab5ca2">MI_SubscriptionDeliveryOptions_GetOptionCount</a>.


#### - GetString

Gets the value of the named string option. See <a href="https://msdn.microsoft.com/5adbbe2a-2cfa-4d24-97e8-5a5d02a685e3">MI_SubscriptionDeliveryOptions_GetString</a>.


#### - SetDateTime

Sets the value of a named DateTime option. See <a href="https://msdn.microsoft.com/d6f2820e-19f2-42b9-876b-4ceb09ea2db5">MI_SubscriptionDeliveryOptions_SetDateTime</a>.


#### - SetInterval

Sets the value of a named interval option. See <a href="https://msdn.microsoft.com/00b6dcbb-be09-464e-af7e-45dac4d70286">MI_SubscriptionDeliveryOptions_SetInterval</a>.


#### - SetNumber

Sets the value of a named numeric option. See <a href="https://msdn.microsoft.com/872af4f8-67e2-4e41-a629-180172dbdd17">MI_SubscriptionDeliveryOptions_SetNumber</a>.


#### - SetString

Sets the value of a named string option. See <a href="https://msdn.microsoft.com/c2bcf5b7-24c1-43cd-bf65-18ad891be7b8">MI_SubscriptionDeliveryOptions_SetString</a>.

