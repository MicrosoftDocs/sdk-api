---
UID: NE:nvme.NVME_ASYNC_EVENT_HEALTH_STATUS_CODES
tech.root: fs
title: NVME_ASYNC_EVENT_HEALTH_STATUS_CODES
ms.date: 03/06/2025
ms.topic: language-reference
targetos: Windows
description: Contains values that indicate a SMART/Health Status event type.
req.construct-type: enumeration
req.ddi-compliance: 
req.header: nvme.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - NVME_ASYNC_EVENT_HEALTH_STATUS_CODES
f1_keywords:
 - NVME_ASYNC_EVENT_HEALTH_STATUS_CODES
 - nvme/NVME_ASYNC_EVENT_HEALTH_STATUS_CODES
dev_langs:
 - c++
---

# NVME_ASYNC_EVENT_HEALTH_STATUS_CODES enumeration

## -description

Contains values that indicate a SMART/Health Status event type.

## -enum-fields

### -field NVME_ASYNC_HEALTH_NVM_SUBSYSTEM_RELIABILITY

NVM subsystem reliability has been compromised. This may be due to significant media errors, an internal error, the media being placed in read only mode, or a volatile memory backup device failing.

### -field NVME_ASYNC_HEALTH_TEMPERATURE_THRESHOLD

A temperature is above an over-temperature threshold or below an under-temperature threshold.

### -field NVME_ASYNC_HEALTH_SPARE_BELOW_THRESHOLD

The available spare space has fallen below the threshold.

## -remarks

Use this enumeration to specify values in the **NVME_ASYNC_EVENT_TYPE_HEALTH_STATUS** field of the [NVME_ASYNC_EVENT_TYPES](ne-nvme-nvme_async_event_types.md) enumeration that is used in the Async Event Request Admin command.

## -see-also

[NVME_ASYNC_EVENT_TYPES](ne-nvme-nvme_async_event_types.md)
[NVME_FEATURES](ne-nvme-nvme_features.md)
[NVME_ADMIN_COMMANDS](ne-nvme-nvme_admin_commands.md)
