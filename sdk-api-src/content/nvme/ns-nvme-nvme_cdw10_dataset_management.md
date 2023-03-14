---
UID: NS:nvme.NVME_CDW10_DATASET_MANAGEMENT
tech.root: fs
title: NVME_CDW10_DATASET_MANAGEMENT
ms.date: 08/09/2022
ms.topic: language-reference
targetos: Windows
description: The NVME_CDW10_DATASET_MANAGEMENT structure contains parameters for the Dataset Management command that indicates attributes for ranges of logical blocks.
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
req.typenames: NVME_CDW10_DATASET_MANAGEMENT, *PNVME_CDW10_DATASET_MANAGEMENT
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW10_DATASET_MANAGEMENT
 - NVME_CDW10_DATASET_MANAGEMENT
f1_keywords:
 - PNVME_CDW10_DATASET_MANAGEMENT
 - nvme/PNVME_CDW10_DATASET_MANAGEMENT
 - NVME_CDW10_DATASET_MANAGEMENT
 - nvme/NVME_CDW10_DATASET_MANAGEMENT
dev_langs:
 - c++
---

# NVME_CDW10_DATASET_MANAGEMENT structure

Contains parameters for the Dataset Management command that is used by the host to indicate attributes for ranges of logical blocks. This includes attributes like frequency that data is read or written, access size, and other information that may be used to optimize performance and reliability. This command is advisory; a compliant controller may choose to take no action based on the information provided.

The Dataset Management command uses the Command Dword 10 **CDW10** and Command Dword 11 **CDW11** fields in the **DATASETMANAGEMENT** parameter of the [Command](ns-nvme-nvme_command.md) structure. If the command uses PRPs for the data transfer, then the PRP Entry 1 **PRP1** and PRP Entry 2 **PRP2** fields are used. All other command specific fields are reserved.

The **NVME_CDW10_DATASET_MANAGEMENT** structure is used in the **CDW10** field of the **DATASETMANAGEMENT** parameter of the [Command](ns-nvme-nvme_command.md) structure.


## -description

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.NR

The Number of Ranges (NR) field indicates the number of 16 byte range sets that are specified in the command. This is a 0’s based value.

### -field DUMMYSTRUCTNAME.Reserved

### -field AsUlong

## -remarks

## -see-also

- [NVME_CDW11_DATASET_MANAGEMENT](ns-nvme-nvme_cdw11_dataset_management.md)

