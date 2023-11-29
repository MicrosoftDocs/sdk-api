---
UID: NF:shellhandwriting.ITfHandwriting.GetHandwritingState
tech.root: input_ink
title: ITfHandwriting::GetHandwritingState (shellhandwriting.h)
ms.date: 10/24/2023
targetos: Windows
description: Retrieves the current handwriting state for the Text Services Framework (TSF) thread manager.
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
 - ITfHandwriting::GetHandwritingState
f1_keywords:
 - ITfHandwriting::GetHandwritingState
 - shellhandwriting/ITfHandwriting::GetHandwritingState
dev_langs:
 - c++
helpviewer_keywords:
 - GetHandwritingState
---

# GetHandwritingState function

## -description

Retrieves the current handwriting state for the [Text Services Framework](/windows/win32/tsf/text-services-framework) (TSF) thread manager.

## -parameters

### -param handwritingState [out]

The system handwriting support. The default is TF_HANDWRITING_AUTO.

## -returns

If the method succeeds, it returns **S_OK**. If it fails, it returns an **HRESULT** error code.

## -remarks

## -see-also

[TfHandwritingState enumeration](ne-shellhandwriting-tfhandwritingstate.md)
