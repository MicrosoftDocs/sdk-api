---
UID: NN:shellhandwriting.ITfHandwritingRequest
tech.root: input_ink
title: ITfHandwritingRequest
ms.date: 11/13/2023
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

## -see-also
