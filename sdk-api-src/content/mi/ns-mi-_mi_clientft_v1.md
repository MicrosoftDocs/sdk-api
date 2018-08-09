---
UID: NS:mi._MI_ClientFT_V1
title: "_MI_ClientFT_V1"
author: windows-sdk-content
description: Client function tables.
old-location: wmi_v2\mi_clientft_v1.htm
old-project: wmi_v2
ms.assetid: 9c8c812d-d91d-4754-9be5-c05360364b1b
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: MI_ClientFT_V1, MI_ClientFT_V1 structure [Windows Management Infrastructure (MI)], _MI_ClientFT_V1, mi/MI_ClientFT_V1, mi/mi_clientFT_V1, mi_clientFT_V1, mi_clientFT_V1 structure pointer [Windows Management Infrastructure (MI)], wmi._mi_clientft_v1, wmi_v2.mi_clientft_v1
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
req.typenames: MI_ClientFT_V1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_ClientFT_V1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MI_ClientFT_V1 structure


## -description


Client function tables.


## -struct-fields




### -field applicationFT

Pointer to the <a href="https://msdn.microsoft.com/0c7d3902-a180-4d71-a223-8f8a68bc9d0b">MI_ApplicationFT</a> function table 
      used by <a href="https://msdn.microsoft.com/da486ade-88ef-40c4-8151-356e718da7db">MI_Application</a>.


### -field sessionFT

Pointer to the <b>MI_SessionFT</b> function table used by 
      <a href="https://msdn.microsoft.com/68a69321-0aa9-423e-a72f-aa2f4dee2d51">MI_Session</a>.


### -field operationFT

Pointer to the <a href="https://msdn.microsoft.com/925cd972-61fc-466d-a2a6-e315ef3fc499">MI_OperationFT</a> function table 
      used by <a href="https://msdn.microsoft.com/a62b3656-c281-4f30-9690-de453df9f2db">MI_Operation</a>.


### -field hostedProviderFT

Pointer to the <a href="https://msdn.microsoft.com/148c4f5a-277a-41fa-b801-34884fbf3225">MI_HostedProviderFT</a> function 
      table used by <a href="https://msdn.microsoft.com/e63283b4-82eb-4bf4-a2f8-f7db29ccb6da">MI_HostedProvider</a>.


### -field serializerFT

Pointer to the <a href="https://msdn.microsoft.com/bf97fff0-0a3d-4326-90a4-c329a06d5741">MI_SerializerFT</a> function table 
      used by <a href="https://msdn.microsoft.com/396b01f2-5238-4cc1-baf2-b602967e4333">MI_Serializer</a>.


### -field deserializerFT

Pointer to the <a href="https://msdn.microsoft.com/dcd2b458-7c25-47a8-a324-43fc1456fcec">MI_DeserializerFT</a> function 
      table used by <a href="https://msdn.microsoft.com/0d2d8f3b-9567-418f-a789-a34b85c114fd">MI_Deserializer</a>.


### -field subscribeDeliveryOptionsFT

Pointer to the 
      <a href="https://msdn.microsoft.com/b6f5406a-2abe-4cab-b257-185d77e1fb0e">MI_SubscriptionDeliveryOptionsFT</a> 
      function table used by 
      <a href="https://msdn.microsoft.com/aaed635c-ee53-4307-a5b4-e9d3bd2e7c21">MI_SubscriptionDeliveryOptions</a>.


### -field destinationOptionsFT

Pointer to the <a href="https://msdn.microsoft.com/e6cf4d82-8820-40d5-924a-e4270252807d">MI_DestinationOptionsFT</a> 
      function table used by 
      <a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a>.


### -field operationOptionsFT

Pointer to the <a href="https://msdn.microsoft.com/ed84d3bc-2cb0-4052-902d-96a3ab3a3ba4">MI_OperationOptionsFT</a> 
      function table used by 
      <a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a>.


### -field utilitiesFT

Pointer to the <a href="https://msdn.microsoft.com/4f82b7b3-833c-42e8-a80c-2d057fc34fe4">MI_UtilitiesFT</a> function 
      table.

