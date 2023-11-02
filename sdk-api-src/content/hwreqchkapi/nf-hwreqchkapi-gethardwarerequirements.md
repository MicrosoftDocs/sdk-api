---
UID: NF:hwreqchkapi.GetHardwareRequirements
tech.root: hwreqchk
title: GetHardwareRequirements (hwreqchkapi.h)
ms.date: 04/24/2023
targetos: Windows
description: Returns a collection of defined hardware requirements for all product-types.
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
 - GetHardwareRequirements
f1_keywords:
 - GetHardwareRequirements
 - hwreqchkapi/GetHardwareRequirements
dev_langs:
 - c++
helpviewer_keywords:
 - GetHardwareRequirements
---

## -description

This API returns a collection of defined hardware requirements for all product-types.

## -parameters

### -param deviceHardwareRequirements

Returns the list of all defined hardware requirements. Any of the hardware requirements returned can be used to evaluate the hardware requirements.

>[!NOTE]
>Internally, the API allocates memory for this argument using **CoTaskMemAlloc** and it is the responsibility of the caller to free the memory using **CoTaskMemFree**.

### -param requirementCount

The number of **HWREQCHK_DEVICE_HARDWARE_REQUIREMENT** items that are returned in *deviceHardwareRequirements*.

## -returns

Returns an `HRESULT` value that indicates the success or failure of the call.

## -remarks

## -see-also
