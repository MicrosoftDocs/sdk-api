---
UID: NE:shellhandwriting.TfProximateHandwritingTargetResponse
tech.root: input_ink
title: TfProximateHandwritingTargetResponse
ms.date: 11/13/2023
targetos: Windows
description: Specifies the supported handwriting behaviors based on the proximate location of a handwriting target object.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: shellhandwriting.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
typedef_isUnnamed: false
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - shellhandwriting.h
api_name:
 - TfProximateHandwritingTargetResponse
f1_keywords:
 - TfProximateHandwritingTargetResponse
 - shellhandwriting/TfProximateHandwritingTargetResponse
dev_langs:
 - c++
helpviewer_keywords:
 - TfProximateHandwritingTargetResponse
---

# TfProximateHandwritingTargetResponse enumeration

## -description

Specifies the supported handwriting behaviors based on the proximate location of a handwriting target object.

## -enum-fields

### -field TF_NO_HANDWRITING_TARGET_PROXIMATE

No valid handwriting target is proximate to the target point and the input should be released for non-handwriting purposes.

### -field TF_HANDWRITING_TARGET_PROXIMATE

There is a valid handwriting target proximate to the target point and the system should start the handwriting experience.

### -field TF_USE_SYSTEM_TARGETING

Unable to determine whether a valid handwriting target is proximate so the system should perform default determination logic (the [IHandwritingInputRoutingCallback interface](nn-shellhandwriting-ihandwritinginputroutingcallback.md) implementation is still called).

### -field TF_USE_POINTER_DELIVERY

Use pointer input for the handwriting experience.

## -remarks

## -see-also
