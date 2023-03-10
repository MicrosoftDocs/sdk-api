---
UID: NE:evcoll._EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS
title: EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS (evcoll.h)
description: Specifies the status of a subscription or an event source with respect to a subscription.
helpviewer_keywords: ["EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS","EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS enumeration","EcRuntimeStatusActiveStatusActive","EcRuntimeStatusActiveStatusDisabled","EcRuntimeStatusActiveStatusInactive","EcRuntimeStatusActiveStatusTrying","evcoll/EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS","evcoll/EcRuntimeStatusActiveStatusActive","evcoll/EcRuntimeStatusActiveStatusDisabled","evcoll/EcRuntimeStatusActiveStatusInactive","evcoll/EcRuntimeStatusActiveStatusTrying","wec.ec_subscription_runtime_status_active_status","wes.ec_subscription_runtime_status_active_status"]
old-location: wec\ec_subscription_runtime_status_active_status.htm
tech.root: WEC
ms.assetid: 254305fe-5646-4661-98e2-b02f5d240da1
ms.date: 12/05/2018
ms.keywords: EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS, EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS enumeration, EcRuntimeStatusActiveStatusActive, EcRuntimeStatusActiveStatusDisabled, EcRuntimeStatusActiveStatusInactive, EcRuntimeStatusActiveStatusTrying, evcoll/EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS, evcoll/EcRuntimeStatusActiveStatusActive, evcoll/EcRuntimeStatusActiveStatusDisabled, evcoll/EcRuntimeStatusActiveStatusInactive, evcoll/EcRuntimeStatusActiveStatusTrying, wec.ec_subscription_runtime_status_active_status, wes.ec_subscription_runtime_status_active_status
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
req.typenames: EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS
 - evcoll/_EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS
 - EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS
 - evcoll/EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS
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
 - EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS
---

# EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS enumeration


## -description

The <b>EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS</b> enumeration specifies the status of a subscription or an event source with respect to a subscription.

## -enum-fields

### -field EcRuntimeStatusActiveStatusDisabled:1

The subscription or event source is disabled.

### -field EcRuntimeStatusActiveStatusActive

The subscription or event source is running.

### -field EcRuntimeStatusActiveStatusInactive

The subscription or event source is inactive. You can query the System event log to see the error events sent by the Event Collector service. Use the <a href="/windows/win32/api/evcoll/ne-evcoll-ec_subscription_runtime_status_info_id">EC_SUBSCRIPTION_RUNTIME_STATUS_INFO_ID</a> values to obtain information on why the subscription or source is inactive.

### -field EcRuntimeStatusActiveStatusTrying

The subscription or event source is trying to connect for the first time or is retrying after a problem. When an active subscription runs into a problem, it will retry several times.

