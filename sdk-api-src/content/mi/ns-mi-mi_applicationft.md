---
UID: NS:mi._MI_ApplicationFT
title: MI_ApplicationFT (mi.h)
description: A support structure used in the MI_Application structure. Use the functions with the name prefix &quot;MI_Application_&quot; to manipulate these structures.
helpviewer_keywords: ["MI_ApplicationFT","MI_ApplicationFT structure [Windows Management Infrastructure (MI)]","mi/MI_ApplicationFT","wmi_v2.mi_applicationft"]
old-location: wmi_v2\mi_applicationft.htm
tech.root: wmi_v2
ms.assetid: 0c7d3902-a180-4d71-a223-8f8a68bc9d0b
ms.date: 12/05/2018
ms.keywords: MI_ApplicationFT, MI_ApplicationFT structure [Windows Management Infrastructure (MI)], mi/MI_ApplicationFT, wmi_v2.mi_applicationft
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
req.typenames: MI_ApplicationFT
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_ApplicationFT
 - mi/_MI_ApplicationFT
 - MI_ApplicationFT
 - mi/MI_ApplicationFT
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
 - MI_ApplicationFT
---

## -description

A support structure used in the <a href="/windows/desktop/api/mi/ns-mi-mi_application">MI_Application</a> structure. Use the functions with the name prefix "MI_Application_" to manipulate these structures.

## -struct-fields

### -field Close

Deinitializes the management infrastructure. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_close">MI_Application_Close</a>.

### -field NewSession

Creates a session that allows a group of operations that go to the same destination to be grouped so they 
       can share connections. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newsession">MI_Application_NewSession</a>.

### -field NewHostedProvider

Creates a new hosted Provider. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newhostedprovider">MI_Application_NewHostedProvider</a>.

### -field NewInstance

Creates an instance. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newinstance">MI_Application_NewInstance</a>.

### -field NewDestinationOptions

Creates an <a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object. 
       See <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>.

### -field NewOperationOptions

Creates an <a href="/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> object. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newoperationoptions">MI_Application_NewOperationOptions</a>.

### -field NewSubscriptionDeliveryOptions

See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newsubscriptiondeliveryoptions">MI_Application_NewSubscriptionDeliveryOptions</a>.

### -field NewSerializer

Creates a serializer allowing a <a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> or an 
       <a href="/windows/desktop/api/mi/ns-mi-mi_class">MI_Class</a> to be persisted in a form that can be stored to 
       disk or transported over a transport. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newserializer">MI_Application_NewSerializer</a>.

### -field NewDeserializer

Creates a deserializer that can be used to re-create the 
       <a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> or 
       <a href="/windows/desktop/api/mi/ns-mi-mi_class">MI_Class</a>. See 
       <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdeserializer">MI_Application_NewDeserializer</a>.

### -field NewInstanceFromClass

TBD

### -field NewClass

TBD
