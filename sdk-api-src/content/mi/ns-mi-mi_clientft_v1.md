---
UID: NS:mi._MI_ClientFT_V1
title: MI_ClientFT_V1 (mi.h)
description: Client function tables.
helpviewer_keywords: ["MI_ClientFT_V1","MI_ClientFT_V1 structure [Windows Management Infrastructure (MI)]","mi/MI_ClientFT_V1","mi/mi_clientFT_V1","mi_clientFT_V1","mi_clientFT_V1 structure pointer [Windows Management Infrastructure (MI)]","wmi._mi_clientft_v1","wmi_v2.mi_clientft_v1"]
old-location: wmi_v2\mi_clientft_v1.htm
tech.root: wmi_v2
ms.assetid: 9c8c812d-d91d-4754-9be5-c05360364b1b
ms.date: 12/05/2018
ms.keywords: MI_ClientFT_V1, MI_ClientFT_V1 structure [Windows Management Infrastructure (MI)], mi/MI_ClientFT_V1, mi/mi_clientFT_V1, mi_clientFT_V1, mi_clientFT_V1 structure pointer [Windows Management Infrastructure (MI)], wmi._mi_clientft_v1, wmi_v2.mi_clientft_v1
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
req.typenames: MI_ClientFT_V1
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_ClientFT_V1
 - mi/_MI_ClientFT_V1
 - MI_ClientFT_V1
 - mi/MI_ClientFT_V1
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
 - MI_ClientFT_V1
---

# MI_ClientFT_V1 structure


## -description

Client function tables.

## -struct-fields

### -field applicationFT

Pointer to the <a href="/windows/desktop/api/mi/ns-mi-mi_applicationft">MI_ApplicationFT</a> function table 
      used by <a href="/windows/desktop/api/mi/ns-mi-mi_application">MI_Application</a>.

### -field sessionFT

Pointer to the <b>MI_SessionFT</b> function table used by 
      <a href="/windows/desktop/api/mi/ns-mi-mi_session">MI_Session</a>.

### -field operationFT

Pointer to the <a href="/windows/desktop/api/mi/ns-mi-mi_operationft">MI_OperationFT</a> function table 
      used by <a href="/windows/desktop/api/mi/ns-mi-mi_operation">MI_Operation</a>.

### -field hostedProviderFT

Pointer to the <a href="/windows/desktop/api/mi/ns-mi-mi_hostedproviderft">MI_HostedProviderFT</a> function 
      table used by <a href="/windows/desktop/api/mi/ns-mi-mi_hostedprovider">MI_HostedProvider</a>.

### -field serializerFT

Pointer to the <a href="/windows/desktop/api/mi/ns-mi-mi_serializerft">MI_SerializerFT</a> function table 
      used by <a href="/windows/desktop/api/mi/ns-mi-mi_serializer">MI_Serializer</a>.

### -field deserializerFT

Pointer to the <a href="/windows/desktop/api/mi/ns-mi-mi_deserializerft">MI_DeserializerFT</a> function 
      table used by <a href="/windows/desktop/api/mi/ns-mi-mi_deserializer">MI_Deserializer</a>.

### -field subscribeDeliveryOptionsFT

Pointer to the 
      <a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptionsft">MI_SubscriptionDeliveryOptionsFT</a> 
      function table used by 
      <a href="/windows/desktop/api/mi/ns-mi-mi_subscriptiondeliveryoptions">MI_SubscriptionDeliveryOptions</a>.

### -field destinationOptionsFT

Pointer to the <a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptionsft">MI_DestinationOptionsFT</a> 
      function table used by 
      <a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a>.

### -field operationOptionsFT

Pointer to the <a href="/windows/desktop/api/mi/ns-mi-mi_operationoptionsft">MI_OperationOptionsFT</a> 
      function table used by 
      <a href="/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a>.

### -field utilitiesFT

Pointer to the <a href="/windows/desktop/api/mi/ns-mi-mi_utilitiesft">MI_UtilitiesFT</a> function 
      table.