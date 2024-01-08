---
UID: NF:shellhandwriting.ITfHandwritingRequest.SetInputEvaluation
tech.root: input_ink
title: ITfHandwritingRequest::SetInputEvaluation
ms.date: 11/14/2023
targetos: Windows
description: Sets how the pen input should be recognized.
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
 - ITfHandwritingRequest::SetInputEvaluation
f1_keywords:
 - ITfHandwritingRequest::SetInputEvaluation
 - shellhandwriting/ITfHandwritingRequest::SetInputEvaluation
dev_langs:
 - c++
helpviewer_keywords:
 - SetInputEvaluation
---

# SetInputEvaluation function

## -description

Sets how the pen input should be recognized.

## -parameters

### -param inputEvaluation [in]

How the pen input should be recognized.

## -returns

If the method succeeds, it returns **S_OK**. If it fails, it returns an **HRESULT** error code.

## -remarks

Once pointer input is deemed to be an ink gesture (such as a tap or press and hold to cancel handwriting), this method must be called after [RequestHandwritingForPointer](nf-shellhandwriting-itfhandwriting-requesthandwritingforpointer.md) when the current handwriting state for the *pointerId* is set to [TF_HANDWRITING_POINTERDELIVERY](ne-shellhandwriting-tfhandwritingstate.md) or [TF_USE_POINTER_DELIVERY](ne-shellhandwriting-tfproximatehandwritingtargetresponse.md) is the response to a handwriting proximity callback.

If a tap is detected, *inputEvaluation* should be set to [TF_IE_TAP](ne-shellhandwriting-tfinputevaluation.md) as this indicates that handwriting corrections should be shown.

If [TF_IE_TAP](ne-shellhandwriting-tfinputevaluation.md) or [TF_IE_CANCELHANDWRITING](ne-shellhandwriting-tfinputevaluation.md) are specified, handwriting will be abandoned. As the handwriting state was set to [TF_HANDWRITING_POINTERDELIVERY](ne-shellhandwriting-tfhandwritingstate.md), all pointer input will have already been delivered to the client.

If [TF_IE_HANDWRITING](ne-shellhandwriting-tfhandwritingstate.md) is specified, handwriting recognition will be initiated.

This method must be called within two seconds of calling [RequestHandwritingForPointer](nf-shellhandwriting-itfhandwriting-requesthandwritingforpointer.md). If this method is not called within this two second time frame, the handwriting operation will be abandoned (equivalent to calling this method and specifying [TF_IE_CANCELHANDWRITING](ne-shellhandwriting-tfhandwritingstate.md)).

## -see-also

[TfInputEvaluation enumeration](ne-shellhandwriting-tfinputevaluation.md)