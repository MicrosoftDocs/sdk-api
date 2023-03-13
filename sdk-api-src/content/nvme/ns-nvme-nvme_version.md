---
UID: NS:nvme.NVME_VERSION
tech.root: fs
title: NVME_VERSION
ms.date: 02/19/2021
ms.topic: language-reference
targetos: Windows
description: Contains fields that specify the version number of the NVM Express specification that the controller implementation supports.
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
req.typenames: NVME_VERSION, *PNVME_VERSION
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - nvme.h
api_name:
 - PNVME_VERSION
 - NVME_VERSION
f1_keywords:
 - PNVME_VERSION
 - nvme/PNVME_VERSION
 - NVME_VERSION
 - nvme/NVME_VERSION
dev_langs:
 - c++
---

# NVME_VERSION structure


## -description

Contains fields that specify the version number of the NVM Express specification that the controller implementation supports.

This structure is used in the **VS** field of the [NVME_CONTROLLER_REGISTERS](../nvme/ns-nvme-nvme_controller_registers.md) structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.TER

Indicates the tertiary version number of the specification.

For example, if the version number is 1.2.3, then 3 is the tertiary version number.

### -field DUMMYSTRUCTNAME.MNR

Indicates the minor version number of the specification.

For example, if the version number is 1.2, then 2 is the minor version number.

### -field DUMMYSTRUCTNAME.MJR

Indicates the major version number of the specification.

For example, if the version number is 1.2, then 1 is the major version number.

### -field AsUlong

## -remarks

Valid versions of the NVM Express specification are: 1.0, 1.1, and 1.2.

## -see-also

