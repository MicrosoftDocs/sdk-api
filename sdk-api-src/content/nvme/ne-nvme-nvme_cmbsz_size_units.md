---
UID: NE:nvme.NVME_CMBSZ_SIZE_UNITS
tech.root: fs
title: NVME_CMBSZ_SIZE_UNITS
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains values that specify the size units that indicate the size of the Controller Memory Buffer.
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
 - NVME_CMBSZ_SIZE_UNITS
f1_keywords:
 - NVME_CMBSZ_SIZE_UNITS
 - nvme/NVME_CMBSZ_SIZE_UNITS
dev_langs:
 - c++
---

# NVME_CMBSZ_SIZE_UNITS enumeration


## -description

Contains values that specify the size units that indicate the size of the Controller Memory Buffer.

## -enum-fields

### -field NVME_CMBSZ_SIZE_UNITS_4KB

The buffer size is in units of 4 KB.

### -field NVME_CMBSZ_SIZE_UNITS_64KB

The buffer size is in units of 64 KB.

### -field NVME_CMBSZ_SIZE_UNITS_1MB

The buffer size is in units of 1 MB.

### -field NVME_CMBSZ_SIZE_UNITS_16MB

The buffer size is in units of 16 MB.

### -field NVME_CMBSZ_SIZE_UNITS_256MB

The buffer size is in units of 256 MB.

### -field NVME_CMBSZ_SIZE_UNITS_4GB

The buffer size is in units of 4 GB.

### -field NVME_CMBSZ_SIZE_UNITS_64GB

The buffer size is in units of 64 GB.

## -remarks

The size of the Controller Memory Buffer indicated in the **SZ** member of the [NVME_CONTROLLER_MEMORY_BUFFER_SIZE](ns-nvme-nvme_controller_memory_buffer_size.md) structure is expressed in multiples of the size units value specified in the **SZU** member (offset 3Ch).

## -see-also

[NVME_CONTROLLER_MEMORY_BUFFER_SIZE](ns-nvme-nvme_controller_memory_buffer_size.md) structure

