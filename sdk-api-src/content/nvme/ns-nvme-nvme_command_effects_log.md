---
UID: NS:nvme.NVME_COMMAND_EFFECTS_LOG
tech.root: fs
title: NVME_COMMAND_EFFECTS_LOG
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains information that describes the commands that the controller supports and the effects of those commands on the state of the NVM subsystem.
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
req.typenames: NVME_COMMAND_EFFECTS_LOG, *PNVME_COMMAND_EFFECTS_LOG
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_COMMAND_EFFECTS_LOG
 - NVME_COMMAND_EFFECTS_LOG
f1_keywords:
 - PNVME_COMMAND_EFFECTS_LOG
 - nvme/PNVME_COMMAND_EFFECTS_LOG
 - NVME_COMMAND_EFFECTS_LOG
 - nvme/NVME_COMMAND_EFFECTS_LOG
dev_langs:
 - c++
---

# NVME_COMMAND_EFFECTS_LOG structure


## -description

Contains information that describes the commands that the controller supports and the effects of those commands on the state of the NVM subsystem.

The Command Effects log page is 4096 bytes in size. There is one [NVME_COMMAND_EFFECTS_DATA](ns-nvme-nvme_command_effects_data.md) structure per Admin command and one per I/O command (based on the I/O Command Set selected in the **CSS** field of the [NVME_CONTROLLER_CONFIGURATION](ns-nvme-nvme_controller_configuration.md) structure).

## -struct-fields

### -field ACS

A [NVME_COMMAND_EFFECTS_DATA](ns-nvme-nvme_command_effects_data.md) structure that describes the Admin commands that the controller supports and the effects of those commands.

### -field IOCS

A [NVME_COMMAND_EFFECTS_DATA](ns-nvme-nvme_command_effects_data.md) structure that describes the I/O commands that the controller supports and the effects of those commands.

### -field Reserved

## -remarks

## -see-also

