---
UID: NS:nvme.NVME_CDW11_DATASET_MANAGEMENT
tech.root: fs
title: NVME_CDW11_DATASET_MANAGEMENT
ms.date: 08/09/2022
ms.topic: language-reference
targetos: Windows
description: The NVME_CDW11_DATASET_MANAGEMENT structure contains parameters for the Dataset Management command that indicates attributes for ranges of logical blocks.
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
req.typenames: NVME_CDW11_DATASET_MANAGEMENT, *PNVME_CDW11_DATASET_MANAGEMENT
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW11_DATASET_MANAGEMENT
 - NVME_CDW11_DATASET_MANAGEMENT
f1_keywords:
 - PNVME_CDW11_DATASET_MANAGEMENT
 - nvme/PNVME_CDW11_DATASET_MANAGEMENT
 - NVME_CDW11_DATASET_MANAGEMENT
 - nvme/NVME_CDW11_DATASET_MANAGEMENT
dev_langs:
 - c++
---

# NVME_CDW11_DATASET_MANAGEMENT structure


## -description

Contains parameters for the Dataset Management command that is used by the host to indicate attributes for ranges of logical blocks. This includes attributes like frequency that data is read or written, access size, and other information that may be used to optimize performance and reliability. This command is advisory; a compliant controller may choose to take no action based on the information provided.

The Dataset Management command uses the Command Dword 10 **CDW10** and Command Dword 11 **CDW11** fields in the **DATASETMANAGEMENT** parameter of the [Command](ns-nvme-nvme_command.md) structure. If the command uses PRPs for the data transfer, then the PRP Entry 1 **PRP1** and PRP Entry 2 **PRP2** fields are used. All other command specific fields are reserved.

The **NVME_CDW11_DATASET_MANAGEMENT** structure is used in the **CDW11** field of the **DATASETMANAGEMENT** parameter of the [Command](ns-nvme-nvme_command.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.IDR

The Integral Dataset for Read (IDR) field indicates how the read access of the dataset should be optimized.

If this value is set to `1`, the dataset should be optimized for read access as an integral unit. The host expects to perform operations on all ranges provided as an integral unit for reads, indicating that if a portion of the dataset is read it is expected that all of the ranges in the dataset are going to be read.

### -field DUMMYSTRUCTNAME.IDW

The Integral Dataset for Write (IDW) field indicates how the write access of the dataset should be optimized.

If this value is set to `1`, the dataset should be optimized for write access as an integral unit. The host expects to perform operations on all ranges provided as an integral unit for writes, indicating that if a portion of the dataset is written it is expected that all of the ranges in the dataset are going to be written.

### -field DUMMYSTRUCTNAME.AD

The Deallocate (AD) field indicates how the dataset ranges should be deallocated.

If this value is set to `1`, the NVM subsystem may deallocate all provided ranges. If a read occurs to a deallocated range, the controller will return all zeros, all ones, or the last data written to the associated Logical Block Allocation (LBA). If the deallocated or unwritten logical block error is enabled and a read occurs to a deallocated range, then the read will fail with the Unwritten or Deallocated Logical Block status code.

### -field DUMMYSTRUCTNAME.Reserved

### -field AsUlong

## -remarks

## -see-also

- [NVME_CDW10_DATASET_MANAGEMENT](ns-nvme-nvme_cdw10_dataset_management.md)

