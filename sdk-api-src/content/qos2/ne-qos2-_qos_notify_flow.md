---
UID: NE:qos2._QOS_NOTIFY_FLOW
title: "_QOS_NOTIFY_FLOW"
author: windows-driver-content
description: The QOS_NOTIFY_FLOW enumeration specifies the circumstances that must be present for the QOSNotifyFlow function to send a notification.
old-location: qos\qos_notify_flow.htm
old-project: QOS
ms.assetid: 96072c6e-8282-4373-bb0b-14fbeb5573c3
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: "*PQOS_NOTIFY_FLOW, PQOS_NOTIFY_FLOW, PQOS_NOTIFY_FLOW enumeration pointer [QOS], QOSNotifyAvailable, QOSNotifyCongested, QOSNotifyUncongested, QOS_NOTIFY_FLOW, QOS_NOTIFY_FLOW enumeration [QOS], _QOS_NOTIFY_FLOW, qos.qos_notify_flow, qos2/PQOS_NOTIFY_FLOW, qos2/QOSNotifyAvailable, qos2/QOSNotifyCongested, qos2/QOSNotifyUncongested, qos2/QOS_NOTIFY_FLOW"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: qos2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: QOS_NOTIFY_FLOW, *PQOS_NOTIFY_FLOW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Qos2.h
api_name:
-	QOS_NOTIFY_FLOW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _QOS_NOTIFY_FLOW enumeration


## -description


The <b>QOS_NOTIFY_FLOW</b> enumeration specifies the circumstances that must be present for the <a href="https://msdn.microsoft.com/e6d541fe-2aeb-4969-b138-869754dbdaa3">QOSNotifyFlow</a> function to send a notification.


## -enum-fields




### -field QOSNotifyCongested

Notifications will be sent when congestion is detected.  If the flow is currently congested, a notification may be sent immediately.


### -field QOSNotifyUncongested

Notifications will be sent when the flow is not congested.  If the flow is currently uncongested, a notification may be sent immediately.


### -field QOSNotifyAvailable

Notifications will be sent when the flow's available capacity is sufficient  to allow upgrading it's bandwidth to a specified  capacity.


## -see-also




<a href="https://msdn.microsoft.com/e6d541fe-2aeb-4969-b138-869754dbdaa3">QOSNotifyFlow</a>



<a href="https://msdn.microsoft.com/022fde13-415e-49aa-8df4-472c4eadd6a0">Quality Windows Audio/Video Experience (qWAVE)</a>
 

 

