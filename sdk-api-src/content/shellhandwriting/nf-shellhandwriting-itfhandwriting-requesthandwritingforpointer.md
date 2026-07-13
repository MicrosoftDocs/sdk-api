---
UID: NF:shellhandwriting.ITfHandwriting.RequestHandwritingForPointer
tech.root: input_ink
title: ITfHandwriting::RequestHandwritingForPointer
ms.date: 11/14/2023
targetos: Windows
description: Requests that the specified pointer and ink stroke be used to provide the handwriting experience.
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
 - ITfHandwriting::RequestHandwritingForPointer
f1_keywords:
 - ITfHandwriting::RequestHandwritingForPointer
 - shellhandwriting/ITfHandwriting::RequestHandwritingForPointer
dev_langs:
 - c++
helpviewer_keywords:
 - RequestHandwritingForPointer
---

# RequestHandwritingForPointer function

## -description

Requests that the specified pointer and ink stroke be used for the handwriting experience.

## -parameters

### -param pointerId [in]

The pointer identifier.

### -param handwritingStrokeId [in]

The ink stroke identifier.

You must call [GetHandwritingStrokeIdForPointer](nf-shellhandwriting-gethandwritingstrokeidforpointer.md) to retrieve the unique ID of the stroke started by a [WM_POINTERDOWN](/windows/win32/inputmsg/wm-pointerdown) message.

### -param requestAccepted [out]

True, if the request was accepted; otherwise, false.

### -param request [out]

A pointer to an [ITfHandwritingRequest](nn-shellhandwriting-itfhandwritingrequest.md) object.

## -returns

If the method succeeds, it returns **S_OK**. If it fails, it returns an **HRESULT** error code.

## -remarks

This method can only be called when the current handwriting state for the *pointerId* is set to [TF_HANDWRITING_POINTERDELIVERY](ne-shellhandwriting-tfhandwritingstate.md) or [TF_USE_POINTER_DELIVERY](ne-shellhandwriting-tfproximatehandwritingtargetresponse.md) is the response to a handwriting proximity callback, otherwise it will return E_INVALIDARG.

This method must be called within two seconds of receiving a [WM_POINTERDOWN](/windows/win32/inputmsg/wm-pointerdown) message for *pointerId*. If this method is not called within this two second time frame, S_OK is returned, but *requestAccepted* will be set to false.

## -see-also

[SetHandwritingState](nf-shellhandwriting-itfhandwriting-sethandwritingstate.md)