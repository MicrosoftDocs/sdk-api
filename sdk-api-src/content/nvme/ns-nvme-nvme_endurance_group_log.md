---
UID: NS:nvme.NVME_ENDURANCE_GROUP_LOG
tech.root: fs
title: NVME_ENDURANCE_GROUP_LOG
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains fields that specify the information in an Endurance Group Information log page that indicates the amount of data being read from and written to an Endurance Group.
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
req.typenames: NVME_ENDURANCE_GROUP_LOG, *PNVME_ENDURANCE_GROUP_LOG
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_ENDURANCE_GROUP_LOG
 - NVME_ENDURANCE_GROUP_LOG
f1_keywords:
 - PNVME_ENDURANCE_GROUP_LOG
 - nvme/PNVME_ENDURANCE_GROUP_LOG
 - NVME_ENDURANCE_GROUP_LOG
 - nvme/NVME_ENDURANCE_GROUP_LOG
dev_langs:
 - c++
---

# NVME_ENDURANCE_GROUP_LOG structure


## -description

Contains fields that specify the information in an Endurance Group Information log page that indicates the amount of data being read from and written to an Endurance Group.

This structure is returned by the Get Log Page command. For more information, see [NVME_CDW10_GET_LOG_PAGE](ns-nvme-nvme_cdw10_get_log_page.md).

## -struct-fields

### -field Reserved0

### -field AvailableSpareThreshold

The amount of spare capacity before the threshold is reached, expressed as a normalized percentage (0 to 100).

### -field PercentageUsed

A vendor-specific estimate of the percentage of life used for the NVM set(s) in the Endurance Group, expressed in units of one billion.

### -field Reserved1

A reserved field.

### -field EnduranceEstimate

An estimate of the total number of data bytes written to NVM set(s) in the Endurance Group, expressed in units of one billion.

### -field DataUnitsRead

The total number of data bytes read from NVM set(s) in the Endurance Group, expressed in units of one billion.

### -field DataUnitsWritten

The total number of data bytes written to the NVM sets(s) in the Endurance Group, expressed in units of one billion.

This value only includes data written by the host.

### -field MediaUnitsWritten

The total number of data bytes written to the NVM sets(s) in the Endurance Group, expressed in units of one billion.

This value includes data written by the host and the controller.

### -field Reserved2

A reserved field.

## -remarks

## -see-also

