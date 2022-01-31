---
UID: NE:qos2._QOS_NOTIFY_FLOW
title: QOS_NOTIFY_FLOW (qos2.h)
description: The QOS_NOTIFY_FLOW enumeration specifies the circumstances that must be present for the QOSNotifyFlow function to send a notification.
helpviewer_keywords: ["*PQOS_NOTIFY_FLOW","PQOS_NOTIFY_FLOW","PQOS_NOTIFY_FLOW enumeration pointer [QOS]","QOSNotifyAvailable","QOSNotifyCongested","QOSNotifyUncongested","QOS_NOTIFY_FLOW","QOS_NOTIFY_FLOW enumeration [QOS]","qos.qos_notify_flow","qos2/PQOS_NOTIFY_FLOW","qos2/QOSNotifyAvailable","qos2/QOSNotifyCongested","qos2/QOSNotifyUncongested","qos2/QOS_NOTIFY_FLOW"]
old-location: qos\qos_notify_flow.htm
tech.root: QOS
ms.assetid: 96072c6e-8282-4373-bb0b-14fbeb5573c3
ms.date: 12/05/2018
ms.keywords: '*PQOS_NOTIFY_FLOW, PQOS_NOTIFY_FLOW, PQOS_NOTIFY_FLOW enumeration pointer [QOS], QOSNotifyAvailable, QOSNotifyCongested, QOSNotifyUncongested, QOS_NOTIFY_FLOW, QOS_NOTIFY_FLOW enumeration [QOS], qos.qos_notify_flow, qos2/PQOS_NOTIFY_FLOW, qos2/QOSNotifyAvailable, qos2/QOSNotifyCongested, qos2/QOSNotifyUncongested, qos2/QOS_NOTIFY_FLOW'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: QOS_NOTIFY_FLOW, *PQOS_NOTIFY_FLOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _QOS_NOTIFY_FLOW
 - qos2/_QOS_NOTIFY_FLOW
 - PQOS_NOTIFY_FLOW
 - qos2/PQOS_NOTIFY_FLOW
 - QOS_NOTIFY_FLOW
 - qos2/QOS_NOTIFY_FLOW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Qos2.h
api_name:
 - QOS_NOTIFY_FLOW
---

# QOS_NOTIFY_FLOW enumeration


## -description

The <b>QOS_NOTIFY_FLOW</b> enumeration specifies the circumstances that must be present for the <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qosnotifyflow">QOSNotifyFlow</a> function to send a notification.

## -enum-fields

### -field QOSNotifyCongested:0

Notifications will be sent when congestion is detected.  If the flow is currently congested, a notification may be sent immediately.

### -field QOSNotifyUncongested:1

Notifications will be sent when the flow is not congested.  If the flow is currently uncongested, a notification may be sent immediately.

### -field QOSNotifyAvailable:2       

Notifications will be sent when the flow's available capacity is sufficient to allow upgrading its bandwidth to a specified capacity.

## -see-also

<a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qosnotifyflow">QOSNotifyFlow</a>



<a href="/previous-versions/windows/desktop/qos/quality-windows-audio-video-experience--qwave-">Quality Windows Audio/Video Experience (qWAVE)</a>
