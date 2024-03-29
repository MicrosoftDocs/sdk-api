---
UID: NE:shellhandwriting.TfHandwritingFocusTargetResponse
tech.root: input_ink
title: TfHandwritingFocusTargetResponse
ms.date: 11/13/2023
targetos: Windows
description: Specifies how a client that implements the IHandwritingInputRoutingCallback interface responds when the FocusHandwritingTarget function is called.
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
 - TfHandwritingFocusTargetResponse
f1_keywords:
 - TfHandwritingFocusTargetResponse
 - shellhandwriting/TfHandwritingFocusTargetResponse
dev_langs:
 - c++
helpviewer_keywords:
 - TfHandwritingFocusTargetResponse
---

# TfHandwritingFocusTargetResponse enumeration

## -description

Specifies how a client that implements the [IHandwritingInputRoutingCallback interface](nn-shellhandwriting-ihandwritinginputroutingcallback.md) responds when the [FocusHandwritingTarget function](nf-shellhandwriting-itfhandwritingsink-focushandwritingtarget.md) is called.

## -enum-fields

### -field TF_NO_HANDWRITING_TARGET

A valid target for handwriting wasn't found and the system should not attempt default targeting.

Handwriting is abandoned and all pointer input processed for it is sent to the target application.

### -field TF_HANDWRITING_TARGET_FOCUSED

Focus is set as requested and handwriting recognition can commence.

### -field TF_HANDWRITING_TARGET_FOCUSED_NO_CORRECTIONS

Focus is set as requested and handwriting recognition can commence, but the system should not show the handwriting correction experience.

Handwriting correction UI is displayed when the user taps on text generated by ink recognition and one or more high probability alternative candidates exist (such as "help" for "hello") from which the user can select to replace the generated text. Specifying this field enables applications to provide their own correction experience instead.

### -field TF_PERFORM_SYSTEM_TARGETING

A valid target for handwriting was found but focus is not set and the system should attempt default targeting.

## -remarks

## -see-also
