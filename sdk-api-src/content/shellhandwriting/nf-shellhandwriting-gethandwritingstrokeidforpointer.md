---
UID: NF:shellhandwriting.GetHandwritingStrokeIdForPointer
tech.root: input_ink
title: GetHandwritingStrokeIdForPointer
ms.date: 10/24/2023
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

Clients that have configured <xref:NF:shellhandwriting.ITfHandwriting.SetHandwritingState>

Clients that have configured the handwriting state as Pointer Delivery must call this function to retrieve the unique Id of the stroke being started by a WM_POINTERDOWN message in order to provide that Id to a RequestHandwritingForPointer call.

<xref:NF:shellhandwriting.ITfHandwriting.RequestHandwritingForPointer>

## -see-also

