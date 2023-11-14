---
UID: NF:shellhandwriting.GetHandwritingStrokeIdForPointer
tech.root: input_ink
title: GetHandwritingStrokeIdForPointer
ms.date: 11/13/2023
targetos: Windows
description: Retrieves the unique ID of the ink stroke associated with the specified pointer ID.
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
 - HeaderDef
api_location:
 - shellhandwriting.h
api_name:
 - GetHandwritingStrokeIdForPointer
f1_keywords:
 - GetHandwritingStrokeIdForPointer
 - shellhandwriting/GetHandwritingStrokeIdForPointer
dev_langs:
 - c++
helpviewer_keywords:
 - GetHandwritingStrokeIdForPointer
---

# GetHandwritingStrokeIdForPointer function

## -description

Retrieves the unique ID of the ink stroke associated with the specified pointer ID.

## -parameters

### -param pointerId [in]

The pointer ID associated with the ink stroke.

### -param handwritingStrokeId [out]

The ID of the ink stroke associated with the *pointerId*.

## -returns

If the method succeeds, it returns **S_OK**; otherwise, it returns an **HRESULT** error code.

## -remarks

Clients using the [SetHandwritingState function](nf-shellhandwriting-itfhandwriting-sethandwritingstate.md) to configure the current handwriting state to [TF_HANDWRITING_POINTERDELIVERY](ne-shellhandwriting-tfhandwritingstate.md) must call this function to retrieve the unique ID of the stroke started by a [WM_POINTERDOWN](/windows/win32/inputmsg/wm-pointerdown) message (to pass to the [RequestHandwritingForPointer function](nf-shellhandwriting-itfhandwriting-requesthandwritingforpointer.md)).

This function must be called on the same thread as the one handling the WM_POINTERDOWN message.

## -see-also
