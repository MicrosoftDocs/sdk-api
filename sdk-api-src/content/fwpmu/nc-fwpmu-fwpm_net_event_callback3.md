---
UID: NC:fwpmu.FWPM_NET_EVENT_CALLBACK3
title: FWPM_NET_EVENT_CALLBACK3
description: A callback function for adding custom behavior to the net event subscription process.
tech.root: fwp
ms.date: 05/01/2024
targetos: Windows
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: fwpmu.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - fwpmu.h
api_name:
 - FWPM_NET_EVENT_CALLBACK3
f1_keywords:
 - FWPM_NET_EVENT_CALLBACK3
 - fwpmu/FWPM_NET_EVENT_CALLBACK3
dev_langs:
 - c++
helpviewer_keywords:
 - FWPM_NET_EVENT_CALLBACK3
---

## -description

**FWPM_NET_EVENT_CALLBACK3** is the function signature of a callback function that you implement, and the system calls. The purpose is to add custom behavior to the net event subscription process.

## -parameters

### -param context

Optional context pointer. It contains the value of the *context* parameter of the [FwpmNetEventSubscribe3](/windows/win32/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe3) function.

### -param event

An [FWPM_NET_EVENT4](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event4) structure that contains the event information.

## -remarks

To register your callback function, call [FwpmNetEventSubscribe3](/windows/win32/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe3).

## -see-also
