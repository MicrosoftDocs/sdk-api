---
UID: NE:nvme.NVME_FIRMWARE_ACTIVATE_ACTIONS
tech.root: fs
title: NVME_FIRMWARE_ACTIVATE_ACTIONS
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains values that indicate the action that is taken on the image downloaded by the Firmware Image Download command or on a previously downloaded and placed image.
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
 - NVME_FIRMWARE_ACTIVATE_ACTIONS
f1_keywords:
 - NVME_FIRMWARE_ACTIVATE_ACTIONS
 - nvme/NVME_FIRMWARE_ACTIVATE_ACTIONS
dev_langs:
 - c++
---

# NVME_FIRMWARE_ACTIVATE_ACTIONS enumeration


## -description

Contains values that indicate the action that is taken on the image downloaded by the Firmware Image Download command or on a previously downloaded and placed image.

The values from this enumeration are passed to the Firmware Commit command.

The Firmware Activate command was renamed to the Firmware Commit command in NVME spec v1.2. For a list of Admin commands, see the [NVME_ADMIN_COMMANDS](ne-nvme-nvme_admin_commands.md) enumeration.

## -enum-fields

### -field NVME_FIRMWARE_ACTIVATE_ACTION_DOWNLOAD_TO_SLOT

The downloaded image replaces the image specified by the Firmware Slot field. This image is not activated.

### -field NVME_FIRMWARE_ACTIVATE_ACTION_DOWNLOAD_TO_SLOT_AND_ACTIVATE

The downloaded image replaces the image specified by the Firmware Slot field. This image is activated at the next reset.

### -field NVME_FIRMWARE_ACTIVATE_ACTION_ACTIVATE

The image specified by the Firmware Slot field is activated at the next reset.

### -field NVME_FIRMWARE_ACTIVATE_ACTION_DOWNLOAD_TO_SLOT_AND_ACTIVATE_IMMEDIATE

The image specified by the Firmware Slot field is requested to be activated immediately without reset.

## -remarks

## -see-also

[NVME_ADMIN_COMMANDS](ne-nvme-nvme_admin_commands.md)

