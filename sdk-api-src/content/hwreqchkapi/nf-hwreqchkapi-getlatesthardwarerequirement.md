---
UID: NF:hwreqchkapi.GetLatestHardwareRequirement
tech.root: hwreqchk
title: GetLatestHardwareRequirement (hwreqchkapi.h)
ms.date: 04/24/2023
targetos: Windows
description: Returns the latest defined requirement for a given product type.
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
 - GetLatestHardwareRequirement
f1_keywords:
 - GetLatestHardwareRequirement
 - hwreqchkapi/GetLatestHardwareRequirement
dev_langs:
 - c++
helpviewer_keywords:
 - GetLatestHardwareRequirement
---

## -description

This API returns the latest defined requirement for a given product type.

## -parameters

### -param productType

Specifies the product type for which the latest defined hardware requirement should be returned. Each defined product type enumeration value can have one or more OS releases that are associated with a hardware requirement.

### -param deviceHardwareRequirement

The latest defined hardware requirement for the given *productType*.

## -returns

Returns an `HRESULT` value that indicates the success or failure of the call.

## -remarks

## -see-also
