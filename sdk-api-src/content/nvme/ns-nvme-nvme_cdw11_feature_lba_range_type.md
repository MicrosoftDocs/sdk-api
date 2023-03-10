---
UID: NS:nvme.NVME_CDW11_FEATURE_LBA_RANGE_TYPE
tech.root: fs
title: NVME_CDW11_FEATURE_LBA_RANGE_TYPE
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains a parameter that specifies the number of LBA ranges for the LBA Range Type Feature in the Set Features command.
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
req.typenames: NVME_CDW11_FEATURE_LBA_RANGE_TYPE, *PNVME_CDW11_FEATURE_LBA_RANGE_TYPE
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW11_FEATURE_LBA_RANGE_TYPE
 - NVME_CDW11_FEATURE_LBA_RANGE_TYPE
f1_keywords:
 - PNVME_CDW11_FEATURE_LBA_RANGE_TYPE
 - nvme/PNVME_CDW11_FEATURE_LBA_RANGE_TYPE
 - NVME_CDW11_FEATURE_LBA_RANGE_TYPE
 - nvme/NVME_CDW11_FEATURE_LBA_RANGE_TYPE
dev_langs:
 - c++
---

# NVME_CDW11_FEATURE_LBA_RANGE_TYPE structure


## -description

Contains a parameter that specifies the number of LBA ranges for the LBA Range Type Feature in the Set Features command.

The values from this structure are used in the **LbaRangeType** field of the [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.NUM

Specifies the number of LBA ranges in this command. This is a 0’s based value. This field is used for the Set Features command only and is ignored for the Get Features command.

### -field DUMMYSTRUCTNAME.Reserved0

### -field AsUlong

## -remarks

LBA range information may be used by a driver to determine if it may utilize a particular LBA range; the information is not exposed to higher level software.

This is optional information that is not required for proper behavior of the system. However, it may be utilized to avoid unintended software issues. For example, if the LBA range indicates that it is a RAID volume then a driver that does not have RAID functionality should not utilize that LBA range (including not overwriting the LBA range). The optional information may be utilized by the driver to determine whether the LBA Range should be exposed to higher level software.

## -see-also

- [NVME_LBA_RANGET_TYPE_ENTRY](ns-nvme-nvme_lba_ranget_type_entry.md)
- [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md)

