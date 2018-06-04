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

# _EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS enumeration


## -description


The <b>EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS</b> enumeration specifies the status of a subscription or an event source with respect to a subscription.


## -enum-fields




### -field EcRuntimeStatusActiveStatusDisabled

The subscription or event source is disabled.


### -field EcRuntimeStatusActiveStatusActive

The subscription or event source is running.


### -field EcRuntimeStatusActiveStatusInactive

The subscription or event source is inactive. You can query the System event log to see the error events sent by the Event Collector service. Use the <a href="https://msdn.microsoft.com/cc4e58d5-22cf-4823-be5d-e056f6690a45">EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID</a> values to obtain information on why the subscription or source is inactive.


### -field EcRuntimeStatusActiveStatusTrying

The subscription or event source is trying to connect for the first time or is retrying after a problem. When an active subscription runs into a problem, it will retry several times.

