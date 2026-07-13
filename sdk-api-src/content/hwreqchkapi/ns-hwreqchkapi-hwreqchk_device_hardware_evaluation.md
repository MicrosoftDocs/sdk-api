---
UID: NS:hwreqchkapi.HWREQCHK_DEVICE_HARDWARE_EVALUATION
tech.root: hwreqchk
title: HWREQCHK_DEVICE_HARDWARE_EVALUATION (hwreqchkapi.h)
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
req.typenames: HWREQCHK_DEVICE_HARDWARE_EVALUATION
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
 - HWREQCHK_DEVICE_HARDWARE_EVALUATION
f1_keywords:
 - HWREQCHK_DEVICE_HARDWARE_EVALUATION
 - hwreqchkapi/HWREQCHK_DEVICE_HARDWARE_EVALUATION
dev_langs:
 - c++
helpviewer_keywords:
 - HWREQCHK_DEVICE_HARDWARE_EVALUATION
---

## -description

Contains the results of a single rule check.

## -struct-fields

### -field RuleName

The name of the current rule being checked. The maximum size of the *RuleName* is 64, as defined by **HWREQCHK_MAX_HARDWARE_RULE_NAME**.

### -field Succeeded

Indicates whether the requirements of the rule was met.

## -remarks

## -see-also
