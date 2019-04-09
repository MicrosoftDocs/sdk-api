---
UID: NF:mi.MI_Application_NewSubscriptionDeliveryOptions
title: MI_Application_NewSubscriptionDeliveryOptions function (mi.h)
author: windows-sdk-content
description: Creates an MI_SubscriptionDeliveryOptions object that represents the configuration needed to carry out subscribe operations over certain protocols.
old-location: wmi_v2\mi_application_newsubscriptiondeliveryoptions.htm
tech.root: wmi_v2
ms.assetid: ac84ec09-7d91-42fc-8271-3e0e54bbb788
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MI_Application_NewSubscriptionDeliveryOptions, MI_Application_NewSubscriptionDeliveryOptions function [Windows Management Infrastructure (MI)], mi/MI_Application_NewSubscriptionDeliveryOptions, wmi_v2.mi_application_newsubscriptiondeliveryoptions
ms.topic: function
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
 - MI_Application_NewSubscriptionDeliveryOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_Application_NewSubscriptionDeliveryOptions function


## -description


Creates an <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> object that represents the configuration needed to carry out subscribe operations over certain protocols.


## -parameters




### -param application [in]

A pointer to a handle returned from the <a href="https://msdn.microsoft.com/32696A33-820D-4D01-AF71-DDA1F34EFBE0">MI_Application_Initialize</a> function.


### -param deliveryType [in]

A value of the <a href="https://msdn.microsoft.com/3e1eb580-8f36-4ddb-8d65-7c7e65dd08bb">MI_SubscriptionDeliveryType</a> enumeration that specifies how the indications are delivered.


### -param deliveryOptions [out]

The returned <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> object.


## -returns



This function returns MI_INLINE MI_Result.




## -remarks



When you have finished using the returned <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> object, close it by calling the <a href="https://msdn.microsoft.com/658dcb26-4ba1-42ef-a404-b431d0c92864">MI_SubscriptionDeliveryOptions_Delete</a> function.



