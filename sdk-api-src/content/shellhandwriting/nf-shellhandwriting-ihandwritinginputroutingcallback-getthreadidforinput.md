---
UID: NF:shellhandwriting.IHandwritingInputRoutingCallback.GetThreadIdForInput
tech.root: input_ink
title: IHandwritingInputRoutingCallback::GetThreadIdForInput
ms.date: 11/13/2023
targetos: Windows
description: Retrieves the ID of the message handling thread for the input target UI.
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
 - IHandwritingInputRoutingCallback::GetThreadIdForInput
f1_keywords:
 - IHandwritingInputRoutingCallback::GetThreadIdForInput
 - shellhandwriting/IHandwritingInputRoutingCallback::GetThreadIdForInput
dev_langs:
 - c++
helpviewer_keywords:
 - GetThreadIdForInput
---

# GetThreadIdForInput function

## -description

Retrieves the ID of the message handling thread for the input target UI.

## -parameters

### -param pointerId [in]

The pointer ID associated with the input.

### -param targetScreenPoint [in]

The screen coordinates of the pointer, in pixels.

### -param targetHWnd [in]

The input target.

### -param uiThreadId [out]

The ID for the message handling thread of the input target UI.

## -returns

If this function succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks

## -see-also
