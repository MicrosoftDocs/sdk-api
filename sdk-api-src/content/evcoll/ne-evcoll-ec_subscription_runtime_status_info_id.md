---
UID: NE:evcoll._EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID
title: EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID (evcoll.h)
description: The EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID enumeration specifies the values used to get the status of a subscription or the status of a particular event source with respect to a subscription.
helpviewer_keywords: ["EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID","EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID enumeration","EcSubscriptionRunTimeStatusActive","EcSubscriptionRunTimeStatusEventSources","EcSubscriptionRunTimeStatusLastError","EcSubscriptionRunTimeStatusLastErrorMessage","EcSubscriptionRunTimeStatusLastErrorTime","EcSubscriptionRunTimeStatusLastHeartbeatTime","EcSubscriptionRunTimeStatusNextRetryTime","evcoll/EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID","evcoll/EcSubscriptionRunTimeStatusActive","evcoll/EcSubscriptionRunTimeStatusEventSources","evcoll/EcSubscriptionRunTimeStatusLastError","evcoll/EcSubscriptionRunTimeStatusLastErrorMessage","evcoll/EcSubscriptionRunTimeStatusLastErrorTime","evcoll/EcSubscriptionRunTimeStatusLastHeartbeatTime","evcoll/EcSubscriptionRunTimeStatusNextRetryTime","wec.ec_subscription_runtime_status_info_id","wes.ec_subscription_runtime_status_info_id"]
old-location: wec\ec_subscription_runtime_status_info_id.htm
tech.root: WEC
ms.assetid: cc4e58d5-22cf-4823-be5d-e056f6690a45
ms.date: 12/05/2018
ms.keywords: EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID, EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID enumeration, EcSubscriptionRunTimeStatusActive, EcSubscriptionRunTimeStatusEventSources, EcSubscriptionRunTimeStatusLastError, EcSubscriptionRunTimeStatusLastErrorMessage, EcSubscriptionRunTimeStatusLastErrorTime, EcSubscriptionRunTimeStatusLastHeartbeatTime, EcSubscriptionRunTimeStatusNextRetryTime, evcoll/EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID, evcoll/EcSubscriptionRunTimeStatusActive, evcoll/EcSubscriptionRunTimeStatusEventSources, evcoll/EcSubscriptionRunTimeStatusLastError, evcoll/EcSubscriptionRunTimeStatusLastErrorMessage, evcoll/EcSubscriptionRunTimeStatusLastErrorTime, evcoll/EcSubscriptionRunTimeStatusLastHeartbeatTime, evcoll/EcSubscriptionRunTimeStatusNextRetryTime, wec.ec_subscription_runtime_status_info_id, wes.ec_subscription_runtime_status_info_id
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
targetos: Windows
req.typenames: EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID
 - evcoll/_EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID
 - EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID
 - evcoll/EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Evcoll.h
api_name:
 - EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID
---

# EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID enumeration


## -description

The <b>EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID</b> enumeration specifies the values used to get the status of a subscription or the status of a particular event source with respect to a subscription. 

 The values are used in the <a href="/windows/desktop/api/evcoll/nf-evcoll-ecgetsubscriptionruntimestatus">EcGetSubscriptionRunTimeStatus</a> function.

## -enum-fields

### -field EcSubscriptionRunTimeStatusActive:0

Get the status of an active or inactive subscription or an event source. This will return an unsigned 32-bit integer value from the <a href="/windows/win32/api/evcoll/ne-evcoll-ec_subscription_runtime_status_active_status">EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS</a> enumeration.

### -field EcSubscriptionRunTimeStatusLastError

Get the last error status of a  subscription or an event source. This will return an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeUInt32</a> value.

### -field EcSubscriptionRunTimeStatusLastErrorMessage

Get the last error message for a  subscription or an event source. This will return an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeString</a> value.

### -field EcSubscriptionRunTimeStatusLastErrorTime

Get the time that the last error occurred for a  subscription or an event source. This will return an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeDateTime</a> value.

### -field EcSubscriptionRunTimeStatusNextRetryTime

Get the next time that the subscription or an event source will try to run (after an error). This will return an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeDateTime</a> value.

### -field EcSubscriptionRunTimeStatusEventSources

Get the event sources for the subscription. For collector initiated subscriptions, this list will be identical to the one in the subscription's configuration.  For source initiated subscriptions, this list will be the set of event sources that collector has heard from in the last 30 days.  This list is persistent across reboots of the event collector. This will return an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeString</a> value.

### -field EcSubscriptionRunTimeStatusLastHeartbeatTime

Get the last time that a heartbeat (a signal used to signify the subscription is working) occurred for a subscription or an event source. This will return an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeDateTime</a> value.

### -field EcSubscriptionRunTimeStatusInfoIdEND
