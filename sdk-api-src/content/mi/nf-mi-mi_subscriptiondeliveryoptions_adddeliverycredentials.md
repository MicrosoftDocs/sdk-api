---
UID: NF:mi.MI_SubscriptionDeliveryOptions_AddDeliveryCredentials
title: MI_SubscriptionDeliveryOptions_AddDeliveryCredentials function
author: windows-sdk-content
description: Sets a subscription option for delivery credentials to use when connecting back to the client to deliver a push indication result.
old-location: wmi_v2\mi_subscriptiondeliveryoptions_adddeliverycredentials.htm
old-project: wmi_v2
ms.assetid: ce531ffb-adaa-49df-a051-da51e04196b3
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: MI_SubscriptionDeliveryOptions_AddDeliveryCredentials, MI_SubscriptionDeliveryOptions_AddDeliveryCredentials function [Windows Management Infrastructure (MI)], mi/MI_SubscriptionDeliveryOptions_AddDeliveryCredentials, wmi_v2.mi_subscriptiondeliveryoptions_adddeliverycredentials
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: MI_Type
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_SubscriptionDeliveryOptions_AddDeliveryCredentials
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_SubscriptionDeliveryOptions_AddDeliveryCredentials function


## -description


Sets a subscription option for delivery credentials to use when connecting back to the client to deliver a push indication result.


## -parameters




### -param self [in, out]

A pointer to a <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a> structure.


### -param value [in]

A pointer to a <a href="https://msdn.microsoft.com/30191cd1-00de-42ef-ac95-5e174d273c80">MI_UserCredentials</a> structure.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



This setting is only used by <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a> (WinRM). The currently supported authentication modes are IssuerCert and Kerberos.



