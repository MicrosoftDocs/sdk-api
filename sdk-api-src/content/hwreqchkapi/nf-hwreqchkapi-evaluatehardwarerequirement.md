---
UID: NF:hwreqchkapi.EvaluateHardwareRequirement
tech.root: hwreqchk
title: EvaluateHardwareRequirement (hwreqchkapi.h)
ms.date: 04/24/2023
targetos: Windows
description: Evaluates a specific requirement and returns a pass or fail result informing the caller whether the device meets the hardware requirement.
prerelease: true
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: HWREQCHK.DLL
req.header: hwreqchkapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: HWREQCHK.LIB
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - hwreqchkapi.h
api_name:
 - EvaluateHardwareRequirement
f1_keywords:
 - EvaluateHardwareRequirement
 - hwreqchkapi/EvaluateHardwareRequirement
dev_langs:
 - c++
helpviewer_keywords:
 - EvaluateHardwareRequirement
---

## -description

This API evaluates a specific requirement and returns a pass or fail result informing the caller whether the device meets the hardware requirement.

## -parameters

### -param hardwareRequirement

Specifies a single and specific requirement that is to be evaluated against.

### -param evaluationResult

The evaluation result. If the device meets hardware requirements, a value of `TRUE` is returned; otherwise, the value is `FALSE`.

### -param constraintsEvaluated

An optional `out` value that returns the list of constraints that were used to evaluate the specific *hardwareRequirement*. Each **HWREQCHK_DEVICE_HARDWARE_EVALUATION** in the array represents a single constraint that was evaluated.

>[!NOTE]
>Internally, the API allocates memory for this argument using **CoTaskMemAlloc** and it is the responsibility of the caller to free the memory using **CoTaskMemFree**.

### -param constraintEvaluationCount

The number of constraints evaluated that are returned in *constraintsEvaluated*.

## -returns

Returns an `HRESULT` value that indicates the success or failure of the call.

## -remarks

## -see-also
