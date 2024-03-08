---
UID: NS:hwreqchkapi.HWREQCHK_DEVICE_HARDWARE_REQUIREMENT
tech.root: hwreqchk
title: HWREQCHK_DEVICE_HARDWARE_REQUIREMENT (hwreqchkapi.h)
ms.date: 04/24/2023
targetos: Windows
description: Contains the results of a single hardware requirement check.
prerelease: true
req.construct-type: structure
req.ddi-compliance: 
req.dll: HWREQCHK.DLL
req.header: hwreqchkapi.h
req.include-header: 
req.kmdf-ver: 
req.lib: HWREQCHK.LIB
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: HWREQCHK_DEVICE_HARDWARE_REQUIREMENT
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - hwreqchkapi.h
api_name:
 - HWREQCHK_DEVICE_HARDWARE_REQUIREMENT
f1_keywords:
 - HWREQCHK_DEVICE_HARDWARE_REQUIREMENT
 - hwreqchkapi/HWREQCHK_DEVICE_HARDWARE_REQUIREMENT
dev_langs:
 - c++
helpviewer_keywords:
 - HWREQCHK_DEVICE_HARDWARE_REQUIREMENT
---

## -description

Contains the results of a single hardware requirement check.

## -struct-fields

### -field TargetRelease

A **HWREQCHK_TARGET_RELEASE** value that indicates the target release of the device being checked.

### -field ProductType

A **HWREQCHK_PRODUCT_TYPE** value that indicates the product type of the device being checked.

### -field Revision

The revision number of the hardware requirement.

### -field IsLatestRequirementForProductType

Indicates if the hardware requirement is the latest revision for the current product type.

### -field RequirementName

The name of the hardware requirement. The maximum size of the *RequirementName* is 64, as defined by **HWREQCHK_MAX_HARDWARE_REQUIREMENT_NAME**.

## -remarks

## -see-also
