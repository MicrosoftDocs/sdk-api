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

# _EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID enumeration


## -description


The <b>EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID</b> enumeration specifies the values used to get the status of a subscription or the status of a particular event source with respect to a subscription. 

 The values are used in the <a href="https://msdn.microsoft.com/17d9d264-5ae3-4e31-869c-ada0c6c5c53b">EcGetSubscriptionRunTimeStatus</a> function.


## -enum-fields




### -field EcSubscriptionRunTimeStatusActive

Get the status of an active or inactive subscription or an event source. This will return an unsigned 32-bit integer value from the <a href="https://msdn.microsoft.com/254305fe-5646-4661-98e2-b02f5d240da1">EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS</a> enumeration.


### -field EcSubscriptionRunTimeStatusLastError

Get the last error status of a  subscription or an event source. This will return an <a href="https://msdn.microsoft.com/f1f20e33-46b0-458e-ac6c-f890be20c455">EcVarTypeUInt32</a> value.


### -field EcSubscriptionRunTimeStatusLastErrorMessage

Get the last error message for a  subscription or an event source. This will return an <a href="https://msdn.microsoft.com/f1f20e33-46b0-458e-ac6c-f890be20c455">EcVarTypeString</a> value.


### -field EcSubscriptionRunTimeStatusLastErrorTime

Get the time that the last error occurred for a  subscription or an event source. This will return an <a href="https://msdn.microsoft.com/f1f20e33-46b0-458e-ac6c-f890be20c455">EcVarTypeDateTime</a> value.


### -field EcSubscriptionRunTimeStatusNextRetryTime

Get the next time that the subscription or an event source will try to run (after an error). This will return an <a href="https://msdn.microsoft.com/f1f20e33-46b0-458e-ac6c-f890be20c455">EcVarTypeDateTime</a> value.


### -field EcSubscriptionRunTimeStatusEventSources

Get the event sources for the subscription. For collector initiated subscriptions, this list will be identical to the one in the subscription's configuration.  For source initiated subscriptions, this list will be the set of event sources that collector has heard from in the last 30 days.  This list is persistent across reboots of the event collector. This will return an <a href="https://msdn.microsoft.com/f1f20e33-46b0-458e-ac6c-f890be20c455">EcVarTypeString</a> value.


### -field EcSubscriptionRunTimeStatusLastHeartbeatTime

Get the last time that a heartbeat (a signal used to signify the subscription is working) occurred for a subscription or an event source. This will return an <a href="https://msdn.microsoft.com/f1f20e33-46b0-458e-ac6c-f890be20c455">EcVarTypeDateTime</a> value.


### -field EcSubscriptionRunTimeStatusInfoIdEND



