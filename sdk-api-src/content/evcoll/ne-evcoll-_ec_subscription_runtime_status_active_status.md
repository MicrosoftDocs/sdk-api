---
UID: NE:evcoll._EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS
title: "_EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS"
author: windows-sdk-content
description: Specifies the status of a subscription or an event source with respect to a subscription.
old-location: wec\ec_subscription_runtime_status_active_status.htm
old-project: WEC
ms.assetid: 254305fe-5646-4661-98e2-b02f5d240da1
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS, EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS enumeration, EcRuntimeStatusActiveStatusActive, EcRuntimeStatusActiveStatusDisabled, EcRuntimeStatusActiveStatusInactive, EcRuntimeStatusActiveStatusTrying, _EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS, evcoll/EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS, evcoll/EcRuntimeStatusActiveStatusActive, evcoll/EcRuntimeStatusActiveStatusDisabled, evcoll/EcRuntimeStatusActiveStatusInactive, evcoll/EcRuntimeStatusActiveStatusTrying, wec.ec_subscription_runtime_status_active_status, wes.ec_subscription_runtime_status_active_status
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
tech.root: 
req.typenames: EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Evcoll.h
api_name:
-	EC_SUBSCRIPTION_RUNTIME_STATUS_ACTIVE_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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

