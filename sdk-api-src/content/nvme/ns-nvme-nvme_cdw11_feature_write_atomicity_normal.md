---
UID: NS:nvme.NVME_CDW11_FEATURE_WRITE_ATOMICITY_NORMAL
tech.root: fs
title: NVME_CDW11_FEATURE_WRITE_ATOMICITY_NORMAL
ms.date: 02/19/2021 Contains parameters for the Write Atomicity Normal Feature that controls the operation of the Atomic Write Unit Normal (**AWUN**) and Namespace Atomic Write Unit Normal (**NAWUN**) parameters that define the controller’s support for atomic operations.
ms.topic: language-reference
targetos: Windows
description: Contains parameters for the Write Atomicity Normal Feature that controls the operation of the Atomic Write Unit Normal (**AWUN**) and Namespace Atomic Write Unit Normal (**NAWUN**) parameters that define the controller’s support for atomic operations.
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
req.typenames: NVME_CDW11_FEATURE_WRITE_ATOMICITY_NORMAL, *PNVME_CDW11_FEATURE_WRITE_ATOMICITY_NORMAL
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_CDW11_FEATURE_WRITE_ATOMICITY_NORMAL
 - NVME_CDW11_FEATURE_WRITE_ATOMICITY_NORMAL
f1_keywords:
 - PNVME_CDW11_FEATURE_WRITE_ATOMICITY_NORMAL
 - nvme/PNVME_CDW11_FEATURE_WRITE_ATOMICITY_NORMAL
 - NVME_CDW11_FEATURE_WRITE_ATOMICITY_NORMAL
 - nvme/NVME_CDW11_FEATURE_WRITE_ATOMICITY_NORMAL
dev_langs:
 - c++
---

# NVME_CDW11_FEATURE_WRITE_ATOMICITY_NORMAL structure


## -description

Contains parameters for the Write Atomicity Normal Feature that controls the operation of the Atomic Write Unit Normal (**AWUN**) and Namespace Atomic Write Unit Normal (**NAWUN**) parameters that define the controller’s support for atomic operations.

The values from this structure are used in the **WriteAtomicityNormal** field of the [NVME_CDW11_FEATURES](ns-nvme-nvme_cdw11_features.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.DN

Indicates whether normal write atomicity should be disabled by specifying that **AWUN** and **NAWUN** are not required.

When this value is set to `1`, the host specifies that **AWUN** and **NAWUN** are not required and that the controller will only honor Atomic Write Unit Power Fail (**AWUPF**) and Namespace Atomic Write Unit Power Fail (**NAWUPF**).

When this value is cleared to `0`, **AWUN**, **NAWUN**, **AWUPF**, and **NAWUPF** will be honored by the controller.

The **AWUN** and **AWUPF** fields are in the [NVME_IDENTIFY_CONTROLLER_DATA](ns-nvme-nvme_identify_controller_data.md) structure, and the **NAWUN** and **NAWUPF** fields are in the [NVME_IDENTIFY_NAMESPACE_DATA](../nvme/ns-nvme-nvme_identify_namespace_data.md) structure.

### -field DUMMYSTRUCTNAME.Reserved0

### -field AsUlong

## -remarks

## -see-also

- [NVME_IDENTIFY_CONTROLLER_DATA](ns-nvme-nvme_identify_controller_data.md)
- [NVME_IDENTIFY_NAMESPACE_DATA](../nvme/ns-nvme-nvme_identify_namespace_data.md)

