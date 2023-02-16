---
UID: NS:nvme.NVME_CONTROLLER_LIST
tech.root: fs
title: NVME_CONTROLLER_LIST
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains an ordered list of controller identifiers.
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
req.typenames: NVME_CONTROLLER_LIST, *PNVME_CONTROLLER_LIST
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CONTROLLER_LIST
 - NVME_CONTROLLER_LIST
f1_keywords:
 - PNVME_CONTROLLER_LIST
 - nvme/PNVME_CONTROLLER_LIST
 - NVME_CONTROLLER_LIST
 - nvme/NVME_CONTROLLER_LIST
dev_langs:
 - c++
---

# NVME_CONTROLLER_LIST structure


## -description

Contains an ordered list of controller identifiers. Each controller identifier corresponds to the **CNTLID** field of a [NVME_IDENTIFY_CONTROLLER_DATA](ns-nvme-nvme_identify_controller_data.md) structure which defines the capabilities and characteristics of a controller in the NVM subsystem.

Unused entries in the controller list are zero filled.

## -struct-fields

### -field NumberOfIdentifiers

Specifies the number of controller entries in the list.

There may be up to 2047 identifiers in the list. A value of 0 indicates that there are no controllers in the list.

### -field ControllerID

Contains a list of unique controller identifiers.

If the first value in the list is `0h`, the list is empty and there are no controllers in the list.

## -remarks

## -see-also

- [NVME_IDENTIFY_CONTROLLER_DATA](ns-nvme-nvme_identify_controller_data.md)

