---
UID: NN:shellhandwriting.ITfHandwritingRequest
tech.root: input_ink
title: ITfHandwritingRequest
ms.date: 12/02/2025
targetos: Windows
description: Applications must use this interface to notify the system that they have evaluated the pen input that occurred after the handwriting request.
prerelease: false
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: shellhandwriting.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - shellhandwriting.h
api_name:
 - ITfHandwritingRequest
f1_keywords:
 - ITfHandwritingRequest
 - shellhandwriting/ITfHandwritingRequest
dev_langs:
 - c++
helpviewer_keywords:
 - ITfHandwritingRequest
---

# ITfHandwritingRequest interface

## -description

Applications must use this interface to notify the system that they have evaluated the pen input that occurred after the handwriting request.

## -remarks

This interface is provided as an output parameter to the [RequestHandwritingForPointer function](nf-shellhandwriting-itfhandwriting-requesthandwritingforpointer.md) (an instance is returned on each successful handwriting request).

This object is not agile, which means that you need to consider its threading model and marshaling behavior (it must be called from the thread associated with the [Thread Manager](/windows/win32/tsf/thread-manager) object). For more info, see [Processes, Threads, and Apartments](/windows/win32/com/processes--threads--and-apartments).

## -see-also
