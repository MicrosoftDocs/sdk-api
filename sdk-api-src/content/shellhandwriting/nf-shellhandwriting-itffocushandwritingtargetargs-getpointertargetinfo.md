---
UID: NF:shellhandwriting.ITfFocusHandwritingTargetArgs.GetPointerTargetInfo
tech.root: input_ink
title: ITfFocusHandwritingTargetArgs::GetPointerTargetInfo
ms.date: 11/13/2023
targetos: Windows
description: Retrieves details about the top-level target window of the pointer input.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: shellhandwriting.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
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
 - COM
api_location:
 - shellhandwriting.h
api_name:
 - ITfFocusHandwritingTargetArgs::GetPointerTargetInfo
f1_keywords:
 - ITfFocusHandwritingTargetArgs::GetPointerTargetInfo
 - shellhandwriting/ITfFocusHandwritingTargetArgs::GetPointerTargetInfo
dev_langs:
 - c++
helpviewer_keywords:
 - GetPointerTargetInfo
---

# GetPointerTargetInfo function

Retrieves details about the top-level target window of the pointer input.

## -description

## -parameters

### -param targetWindow [out, optional]

The target window of the pointer input.

### -param targetScreenArea [out, optional]

The target area of the pointer input.

This value is based on the dots-per-inch (DPI) awareness of the current thread associated with the Text Services Framework (TSF) thread manager object.

### -param distanceThreshold [out, optional]

The distance (vertical and horizontal) in pixels from a valid edit control for which the *[targetScreenPoint](nf-shellhandwriting-itfdetermineproximatehandwritingtargetargs-getpointertargetinfo.md)* enables handwriting functionality.  

This value is based on the dots-per-inch (DPI) awareness of the current thread associated with the TSF thread manager object.

## -returns

If this function succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks

## -see-also
