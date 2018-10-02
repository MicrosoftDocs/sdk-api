---
UID: NE:evcoll._EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID
title: "_EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID"
author: windows-sdk-content
description: The EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID enumeration specifies the values used to get the status of a subscription or the status of a particular event source with respect to a subscription.
old-location: wec\ec_subscription_runtime_status_info_id.htm
tech.root: WEC
ms.assetid: cc4e58d5-22cf-4823-be5d-e056f6690a45
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID, EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID enumeration, EcSubscriptionRunTimeStatusActive, EcSubscriptionRunTimeStatusEventSources, EcSubscriptionRunTimeStatusLastError, EcSubscriptionRunTimeStatusLastErrorMessage, EcSubscriptionRunTimeStatusLastErrorTime, EcSubscriptionRunTimeStatusLastHeartbeatTime, EcSubscriptionRunTimeStatusNextRetryTime, _EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID, evcoll/EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID, evcoll/EcSubscriptionRunTimeStatusActive, evcoll/EcSubscriptionRunTimeStatusEventSources, evcoll/EcSubscriptionRunTimeStatusLastError, evcoll/EcSubscriptionRunTimeStatusLastErrorMessage, evcoll/EcSubscriptionRunTimeStatusLastErrorTime, evcoll/EcSubscriptionRunTimeStatusLastHeartbeatTime, evcoll/EcSubscriptionRunTimeStatusNextRetryTime, wec.ec_subscription_runtime_status_info_id, wes.ec_subscription_runtime_status_info_id
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: evcoll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - Evcoll.h
api_name:
 - EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID
product: Windows
targetos: Windows
req.typenames: EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID
req.redist: 
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



