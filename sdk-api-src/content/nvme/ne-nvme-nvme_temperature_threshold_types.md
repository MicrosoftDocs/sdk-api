---
UID: NE:nvme.NVME_TEMPERATURE_THRESHOLD_TYPES
tech.root: fs
title: NVME_TEMPERATURE_THRESHOLD_TYPES
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains values that indicate the type of threshold for the temperature of the overall device (controller and NVM included).
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
 - NVME_TEMPERATURE_THRESHOLD_TYPES
f1_keywords:
 - NVME_TEMPERATURE_THRESHOLD_TYPES
 - nvme/NVME_TEMPERATURE_THRESHOLD_TYPES
dev_langs:
 - c++
---

# NVME_TEMPERATURE_THRESHOLD_TYPES enumeration


## -description

Contains values that indicate the type of threshold for the temperature of the overall device (controller and NVM included).

## -enum-fields

### -field NVME_TEMPERATURE_OVER_THRESHOLD

Over Temperature Threshold

### -field NVME_TEMPERATURE_UNDER_THRESHOLD

Under Temperature Threshold

## -remarks

Values from this enumeration are used in the **THSEL** field of the [NVME_CDW11_FEATURE_TEMPERATURE_THRESHOLD](ns-nvme-nvme_cdw11_feature_temperature_threshold.md) structure.

## -see-also

