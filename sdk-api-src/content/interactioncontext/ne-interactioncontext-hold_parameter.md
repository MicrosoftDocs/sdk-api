---
UID: NE:interactioncontext.HOLD_PARAMETER
tech.root: input_intcontext
title: HOLD_PARAMETER enumeration (interactioncontext.h)
ms.date: 06/27/2024
description: Specifies various values relevant to a press and hold gesture.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: interactioncontext.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10 version 21H1
req.target-min-winversvr: Windows Server 2022
req.target-type: Windows
targetos: Windows
req.typenames: 
typedef_isUnnamed: false
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - interactioncontext.h
api_name:
 - HOLD_PARAMETER
f1_keywords:
 - HOLD_PARAMETER
 - interactioncontext/HOLD_PARAMETER
dev_langs:
 - c++
helpviewer_keywords:
 - HOLD_PARAMETER
---

# HOLD_PARAMETER enumeration

## -description

Specifies various values relevant to a press and hold gesture.

## -enum-fields

### -field HOLD_PARAMETER_MIN_CONTACT_COUNT

The minimum number of contacts recognized.

### -field HOLD_PARAMETER_MAX_CONTACT_COUNT

The maximum number of contacts recognized.

### -field HOLD_PARAMETER_THRESHOLD_RADIUS

The radius around the contact point affected by the hold, in DIPs.

### -field HOLD_PARAMETER_THRESHOLD_START_DELAY

The time threshold for when hold is recognized, in milliseconds.

### -field HOLD_PARAMETER_MAX

Maximum number of interactions exceeded.

## -remarks

## -see-also

[GetHoldParameterInteractionContext function](nf-interactioncontext-getholdparameterinteractioncontext.md)

[SetHoldParameterInteractionContext function](nf-interactioncontext-setholdparameterinteractioncontext.md)
