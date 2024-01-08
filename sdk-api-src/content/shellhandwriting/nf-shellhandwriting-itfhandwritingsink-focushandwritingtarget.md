---
UID: NF:shellhandwriting.ITfHandwritingSink.FocusHandwritingTarget
tech.root: input_ink
title: ITfHandwritingSink::FocusHandwritingTarget
ms.date: 10/24/2023
targetos: Windows
description: 
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
 - ITfHandwritingSink::FocusHandwritingTarget
f1_keywords:
 - ITfHandwritingSink::FocusHandwritingTarget
 - shellhandwriting/ITfHandwritingSink::FocusHandwritingTarget
dev_langs:
 - c++
helpviewer_keywords:
 - FocusHandwritingTarget
---

# FocusHandwritingTarget function

## -description

Sets focus to the edit control that receives the input.

## -parameters

### -param focusHandwritingTargetArgs [in]

The event arguments

## -returns

A handle to the edit control that receives the input.

## -remarks

This function is called only when a valid handwriting target is identified through the [DetermineProximateHandwritingTarget function](nf-shellhandwriting-itfhandwritingsink-determineproximatehandwritingtarget.md) and only when handwriting recognition is to be provided for the input.

The application that implements this function is required to set focus to the most likely edit control based on *focusHandwritingTargetArgs*. This control is where the system will insert the result of handwriting recognition.

## -see-also
