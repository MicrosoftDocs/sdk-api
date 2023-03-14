---
UID: NS:nvme.NVME_FIRMWARE_SLOT_INFO_LOG
tech.root: fs
title: NVME_FIRMWARE_SLOT_INFO_LOG
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains fields that specify the information in the Firmware Slot Information log page.
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
req.typenames: NVME_FIRMWARE_SLOT_INFO_LOG, *PNVME_FIRMWARE_SLOT_INFO_LOG
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_FIRMWARE_SLOT_INFO_LOG
 - NVME_FIRMWARE_SLOT_INFO_LOG
f1_keywords:
 - PNVME_FIRMWARE_SLOT_INFO_LOG
 - nvme/PNVME_FIRMWARE_SLOT_INFO_LOG
 - NVME_FIRMWARE_SLOT_INFO_LOG
 - nvme/NVME_FIRMWARE_SLOT_INFO_LOG
dev_langs:
 - c++
---

# NVME_FIRMWARE_SLOT_INFO_LOG structure


## -description

Contains fields that specify the information in the Firmware Slot Information log page.

The Firmware Slot Information log page reports the firmware revision number (as an ASCII string) for each of the supported firmware slots, and indicates the active slot number. This log page is global to the controller.

This structure is returned by the Get Log Page command. For more information, see [NVME_CDW10_GET_LOG_PAGE](ns-nvme-nvme_cdw10_get_log_page.md).

## -struct-fields

### -field AFI

An Active Firmware Information (**AFI**) structure containing fields that specify information about the active firmware revision.

### -field AFI.ActiveSlot

Indicates the firmware slot that contains the actively running firmware revision.

This value is contained in Bits 0:2 of the **AFI** structure.

### -field AFI.Reserved0

Bit 3 of the **AFI** structure is reserved.

### -field AFI.PendingActivateSlot

Indicates the firmware slot that is going to be activated at the next controller reset.

When this field is set to `0h`, the controller does not indicate the firmware slot that is going to be activated at the next controller reset.

This value is contained in bits 4:6 of the **AFI** structure

### -field AFI.Reserved1

Bit 7 of the **AFI** structure is reserved.

### -field Reserved0

### -field FRS

An array of 7 Firmware Revisions that contain the revision of the firmware downloaded to each of the 7 firmware slots.

The members of the array are named based on the firmware slot number (1-7), such that Firmware Revision for Slot 1 (FRS1) is in position 1, Firmware Revision for Slot 2 (FRS2) is in position 2, and so on, up to Firmware Revision for Slot 7 (FRS7) in position 7.

If no valid firmware revision is present, or if a slot is unsupported, all zeros will be returned for that slot.

### -field Reserved1

## -remarks

## -see-also

