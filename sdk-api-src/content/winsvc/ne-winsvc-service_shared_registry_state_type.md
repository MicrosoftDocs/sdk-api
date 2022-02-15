---
UID: NE:winsvc.SERVICE_SHARED_REGISTRY_STATE_TYPE
title: SERVICE_SHARED_REGISTRY_STATE_TYPE
description: Specifies a state type for a service registry key.
tech.root: security
ms.date: 5/24/2021
ms.keywords: SERVICE_SHARED_REGISTRY_STATE_TYPE
targetos: Windows
req.construct-type: enumeration
req.ddi-compliance: 
req.header: winsvc.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10, version 20H2 (10.0; Build 19042)
req.target-min-winversvr: Windows Server, version 20H2 (10.0; Build 19042)
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
 - SERVICE_SHARED_REGISTRY_STATE_TYPE
f1_keywords:
 - SERVICE_SHARED_REGISTRY_STATE_TYPE
 - winsvc/SERVICE_SHARED_REGISTRY_STATE_TYPE
---

## -description

Specifies a state type for a shared service registry key.

## -enum-fields

### -field ServiceSharedRegistryPersistentState:0

Mutable, persistent service state. This state is readable and writeable by the service and by local administrators. This state persists across reboots and and OS updates.

## -remarks

All per-service registry state types have a lifetime that is scoped to the lifetime of the service installation.
Once the service is removed by calling [DeleteService](/windows/win32/api/winsvc/ne-winsvc-DeleteService) the registry state is deleted too.

## -see-also

[GetSharedServiceRegistryStateKey](/windows/win32/api/winsvc/ne-winsvc-getsharedserviceregistrystatekey)

