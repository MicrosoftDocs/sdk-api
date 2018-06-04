---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

