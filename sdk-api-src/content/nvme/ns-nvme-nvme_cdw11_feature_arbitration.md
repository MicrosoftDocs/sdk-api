---
UID: NS:nvme.NVME_CDW11_FEATURE_ARBITRATION
tech.root: fs
title: NVME_CDW11_FEATURE_ARBITRATION
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains values for the Arbitration Feature that controls command arbitration.
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
req.typenames: NVME_CDW11_FEATURE_ARBITRATION, *PNVME_CDW11_FEATURE_ARBITRATION
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW11_FEATURE_ARBITRATION
 - NVME_CDW11_FEATURE_ARBITRATION
f1_keywords:
 - PNVME_CDW11_FEATURE_ARBITRATION
 - nvme/PNVME_CDW11_FEATURE_ARBITRATION
 - NVME_CDW11_FEATURE_ARBITRATION
 - nvme/NVME_CDW11_FEATURE_ARBITRATION
dev_langs:
 - c++
---

# NVME_CDW11_FEATURE_ARBITRATION structure


## -description

Contains values for the Arbitration Feature that controls command arbitration.

The values from this structure are used in the **Arbitration** field of the [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.AB

Specifies the maximum number of commands that the controller may launch at one time from a particular Submission Queue.

The value for this field is specified as 2^n. A value of `111b` indicates no limit. The possible values for this field are 1, 2, 4, 8, 16, 32, 64, or no limit.

### -field DUMMYSTRUCTNAME.Reserved0

### -field DUMMYSTRUCTNAME.LPW

Specifies the Low Priority Weight (LPW). The number of commands that may be executed from the low priority service class in each arbitration round. This is a 0’s based value.

### -field DUMMYSTRUCTNAME.MPW

Specifies the Medium Priority Weight (MPW). The number of commands that may be executed from the medium priority service class in each arbitration round. This is a 0’s based value.

### -field DUMMYSTRUCTNAME.HPW

Specifies the High Priority Weight (HPW). The number of commands that may be executed from the high priority service class in each arbitration round. This is a 0’s based value.

### -field AsUlong

## -remarks

## -see-also

- [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md)

