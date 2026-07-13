---
UID: NE:directml.DML_ROUNDING_MODE
title: DML_ROUNDING_MODE
description: Defines constants that specify a rounding mode.
ms.date: 10/31/2024
tech.root: directml
req.construct-type: enumeration
req.header: directml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
typedef_isUnnamed: false
f1_keywords:
 - DML_ROUNDING_MODE
 - directml/DML_ROUNDING_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DirectML.h
api_name:
 - DML_ROUNDING_MODE
helpviewer_keywords:
 - DML_ROUNDING_MODE
---

## -description

Defines constants that specify a rounding mode.

## -enum-fields

### -field DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN

Specifies rounding to the nearest integer, with tied halves to the nearest even integer.

### -field DML_ROUNDING_MODE_TOWARD_ZERO

Specifies rounding toward zero to the nearest integer.

### -field DML_ROUNDING_MODE_TOWARD_INFINITY

Specifies rounding to the nearest integer, with tied halves toward the nearest infinity / away from zero.

## -remarks

| Original value                           | -2.5 | -1.75 | -1.5 | -1.25 | 0 | 1.25 | 1.5 | 1.75 | 2.5 |
|------------------------------------------|------|-------|------|-------|---|------|-----|------|-----|
| DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN | -2   | -2    | -2   | -1    | 0 | 1    | 2   | 2    | 2   |
| DML_ROUNDING_MODE_TOWARD_ZERO            | -2   | -1    | -1   | -1    | 0 | 1    | 1   | 1    | 2   |
| DML_ROUNDING_MODE_TOWARD_INFINITY        | -3   | -2    | -2   | -1    | 0 | 1    | 2   | 2    | 3   |

## -see-also
