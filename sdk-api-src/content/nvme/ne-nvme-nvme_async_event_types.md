---
UID: NE:nvme.NVME_ASYNC_EVENT_TYPES
tech.root: fs
title: NVME_ASYNC_EVENT_TYPES
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains values that indicate an asynchronous event type.
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
 - NVME_ASYNC_EVENT_TYPES
f1_keywords:
 - NVME_ASYNC_EVENT_TYPES
 - nvme/NVME_ASYNC_EVENT_TYPES
dev_langs:
 - c++
---

# NVME_ASYNC_EVENT_TYPES enumeration


## -description

Contains values that indicate an asynchronous event type.

## -enum-fields

### -field NVME_ASYNC_EVENT_TYPE_ERROR_STATUS

A general error that is not associated with a specific command. The status of this event is one of the values specified in the **NVME_ASYNC_EVENT_ERROR_STATUS_CODES** enumeration.

### -field NVME_ASYNC_EVENT_TYPE_HEALTH_STATUS

A SMART or Health status event. The status of this event is one of the values specified in the **NVME_ASYNC_EVENT_HEALTH_STATUS_CODES** enumeration.

### -field NVME_ASYNC_EVENT_TYPE_NOTICE

A Notice event. The status of this event is one of the values specified in the **NVME_ASYNC_EVENT_NOTICE_CODES** enumeration.

### -field NVME_ASYNC_EVENT_TYPE_IO_COMMAND_SET_STATUS

An I/O Command Set event. The status of this event is one of the values specified in the **NVME_ASYNC_EVENT_IO_COMMAND_SET_STATUS_CODES** enumeration.

### -field NVME_ASYNC_EVENT_TYPE_VENDOR_SPECIFIC

A vendor specific event. The status of this event is one of the values specified in the **NVME_ASYNC_EVENT_TYPE_VENDOR_SPECIFIC_CODES** enumeration.

## -remarks

Use the Event type information values from this enumeration in [Dword 0](ns-nvme-nvme_command_dword0.md) of the Completion Queue entry for an Asynchronous Event Request command.

## -see-also

