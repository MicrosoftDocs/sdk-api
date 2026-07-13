---
UID: NE:nvme.NVME_CSTS_SHST_SHUTDOWN_STATUS
tech.root: fs
title: NVME_CSTS_SHST_SHUTDOWN_STATUS
ms.date: 01/03/2023
ms.topic: language-reference
targetos: Windows
description: Contains values that indicate the status of shutdown processing that is initiated by the host setting the **SHN** field in the [NVME_CONTROLLER_CONFIGURATION](../nvme/ns-nvme-nvme_controller_configuration.md) structure.
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
 - NVME_CSTS_SHST_SHUTDOWN_STATUS
f1_keywords:
 - NVME_CSTS_SHST_SHUTDOWN_STATUS
 - nvme/NVME_CSTS_SHST_SHUTDOWN_STATUS
dev_langs:
 - c++
---

# NVME_CSTS_SHST_SHUTDOWN_STATUS enumeration


## -description

Contains values that indicate the status of shutdown processing that is initiated by the host setting the **SHN** field in the [NVME_CONTROLLER_CONFIGURATION](../nvme/ns-nvme-nvme_controller_configuration.md) structure.

## -enum-fields

### -field NVME_CSTS_SHST_NO_SHUTDOWN

Normal operation (no shutdown has been requested).

### -field NVME_CSTS_SHST_SHUTDOWN_IN_PROCESS

Shutdown processing is occurring.

### -field NVME_CSTS_SHST_SHUTDOWN_COMPLETED

Shutdown processing is complete.

## -remarks

To start executing commands on the controller after a shutdown operation, (when the **SHST** field of the [NVME_CONTROLLER_STATUS](../nvme/ns-nvme-nvme_controller_status.md) structure is set to `10b`, a Controller Reset (setting the **EN** field in [NVME_CONTROLLER_CONFIGURATION](../nvme/ns-nvme-nvme_controller_configuration.md) to `0`) is required. If the host software submits commands to the controller without issuing a reset, the behavior is undefined.

## -see-also

[NVME_CONTROLLER_STATUS](../nvme/ns-nvme-nvme_controller_status.md)
[NVME_CONTROLLER_CONFIGURATION](../nvme/ns-nvme-nvme_controller_configuration.md)

