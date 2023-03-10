---
UID: NE:nvme.NVME_CC_SHN_SHUTDOWN_NOTIFICATIONS
tech.root: fs
title: NVME_CC_SHN_SHUTDOWN_NOTIFICATIONS
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains values that indicate a Controller Configuration (CC) shutdown notification.
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
 - NVME_CC_SHN_SHUTDOWN_NOTIFICATIONS
f1_keywords:
 - NVME_CC_SHN_SHUTDOWN_NOTIFICATIONS
 - nvme/NVME_CC_SHN_SHUTDOWN_NOTIFICATIONS
dev_langs:
 - c++
---

# NVME_CC_SHN_SHUTDOWN_NOTIFICATIONS enumeration


## -description

Contains values that indicate a Controller Configuration (CC) shutdown notification.

## -enum-fields

### -field NVME_CC_SHN_NO_NOTIFICATION

No notification and no effect.

### -field NVME_CC_SHN_NORMAL_SHUTDOWN

Normal shutdown notification.

### -field NVME_CC_SHN_ABRUPT_SHUTDOWN

Abrupt shutdown notification.

## -remarks

Use the CC shutdown notification values from this enumeration in the **SHN** field (offset 14h) of the [NVME_CONTROLLER_CONFIGURATION](ns-nvme-nvme_controller_configuration.md) structure.

## -see-also

[NVME_CONTROLLER_CONFIGURATION](ns-nvme-nvme_controller_configuration.md)

