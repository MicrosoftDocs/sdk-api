---
UID: NS:nvme.NVME_CDW10_FIRMWARE_ACTIVATE
tech.root: fs
title: NVME_CDW10_FIRMWARE_ACTIVATE
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains parameters used in the Firmware Commit command.
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: nvme.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: 
req.target-type: 
req.typenames: NVME_CDW10_FIRMWARE_ACTIVATE, *PNVME_CDW10_FIRMWARE_ACTIVATE
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW10_FIRMWARE_ACTIVATE
 - NVME_CDW10_FIRMWARE_ACTIVATE
f1_keywords:
 - PNVME_CDW10_FIRMWARE_ACTIVATE
 - nvme/PNVME_CDW10_FIRMWARE_ACTIVATE
 - NVME_CDW10_FIRMWARE_ACTIVATE
 - nvme/NVME_CDW10_FIRMWARE_ACTIVATE
dev_langs:
 - c++
---

# NVME_CDW10_FIRMWARE_ACTIVATE structure


## -description

Contains parameters used in the Firmware Commit command.

The Firmware Commit command is used to verify that a valid firmware image has been downloaded and to commit that revision to a specific firmware slot.

> [!NOTE]
> The Firmware Commit command was called Firmware Activate in previous versions of NVM Express.

This structure is used as the value of the **CDW10** parameter in the **FIRMWAREACTIVATE** field of the [Command](ns-nvme-nvme_command.md) structure. All other command specific fields are reserved.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.FS

The Firmware Slot (FS) field specifies the firmware slot that is used for the Commit Action, if applicable. If the value specified is `0h`, then the controller will choose the firmware slot (1 – 7) to use for the operation.

### -field DUMMYSTRUCTNAME.AA

The Activate Action (AA) field specifies the action that is taken on the image downloaded with the Firmware Image Download command or on a previously downloaded and placed image. The actions are indicated by one of the values in the [NVME_FIRMWARE_ACTIVATE_ACTIONS](ne-nvme-nvme_firmware_activate_actions.md) enumeration.

### -field DUMMYSTRUCTNAME.Reserved

### -field AsUlong

## -remarks

## -see-also

