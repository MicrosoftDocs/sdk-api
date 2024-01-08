---
UID: NF:shellhandwriting.ITfHandwriting.GetHandwritingDistanceThreshold
tech.root: input_ink
title: ITfHandwriting::GetHandwritingDistanceThreshold
ms.date: 11/13/2023
targetos: Windows
description: Retrieves the distance (vertical and horizontal) in pixels from a valid edit control for which the targetScreenPoint enables handwriting functionality.
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
 - ITfHandwriting::GetHandwritingDistanceThreshold
f1_keywords:
 - ITfHandwriting::GetHandwritingDistanceThreshold
 - shellhandwriting/ITfHandwriting::GetHandwritingDistanceThreshold
dev_langs:
 - c++
helpviewer_keywords:
 - GetHandwritingDistanceThreshold
---

# GetHandwritingDistanceThreshold function

## -description

Retrieves the distance (vertical and horizontal) in pixels from a valid edit control for which the *[targetScreenPoint](nf-shellhandwriting-itfdetermineproximatehandwritingtargetargs-getpointertargetinfo.md)* enables handwriting functionality.

## -parameters

### -param distanceThresholdPixels [out]

The distance (vertical and horizontal) in pixels from a valid edit control for which the *[targetScreenPoint](nf-shellhandwriting-itfdetermineproximatehandwritingtargetargs-getpointertargetinfo.md)* enables handwriting functionality.

## -returns

If this function succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks

This value is based on the dots-per-inch (DPI) awareness of the current thread associated with the TSF thread manager object.

## -see-also
