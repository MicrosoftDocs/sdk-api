---
UID: NE:winsvc.SERVICE_REGISTRY_STATE_TYPE
title: SERVICE_REGISTRY_STATE_TYPE
description: Specifies a state type for a service registry key.
tech.root: security
ms.date: 4/26/2019
ms.keywords: SERVICE_REGISTRY_STATE_TYPE
targetos: Windows
req.construct-type: enumeration
req.ddi-compliance: 
req.header: winsvc.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - winsvc.h
api_name:
 - SERVICE_REGISTRY_STATE_TYPE
f1_keywords:
 - SERVICE_REGISTRY_STATE_TYPE
 - winsvc/SERVICE_REGISTRY_STATE_TYPE
---

## -description

Specifies a state type for a service registry key.

## -enum-fields

### -field ServiceRegistryStateParameters:0

Immutable service state, populated by INF to the Parameters subkey.

### -field ServiceRegistryStatePersistent:1

Mutable, persistent service state. This state is both readable and writable by the service, and is inaccessible outside of the service. This state persists across reboots and and OS updates.

### -field MaxServiceRegistryStateType:2

Reserved. Represents the maximum value of the enumeration.

## -remarks

All per-service registry state types have a lifetime that is scoped to the lifetime of the service installation.
Once the service is removed by calling [DeleteService](/windows/win32/api/winsvc/ne-winsvc-DeleteService) the registry state is deleted too.

## -see-also

[GetServiceRegistryStateKey](/windows/win32/api/winsvc/ne-winsvc-getserviceregistrystatekey)

