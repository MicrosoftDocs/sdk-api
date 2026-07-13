---
UID: NN:audioenginebaseapo.IApoAuxiliaryInputRT
tech.root: audio
title: IApoAuxiliaryInputRT
ms.date: 02/17/2021
ms.topic: language-reference
targetos: Windows
description: The realtime-safe interface used to drive the auxiliary inputs of an APO.
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: audioenginebaseapo.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: 
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - audioenginebaseapo.h
api_name:
 - IApoAuxiliaryInputRT
f1_keywords:
 - IApoAuxiliaryInputRT
 - audioenginebaseapo/IApoAuxiliaryInputRT
helpviewer_keywords:
 - IApoAuxiliaryInputRT
 - audioenginebaseapo/IApoAuxiliaryInputRT
dev_langs:
 - c++
---

## -description

The realtime-safe interface used to drive the auxiliary inputs of an APO.


## -remarks
This method may be called from a real-time processing thread. The implementation 
of these methods must not block, touch paged memory, or call any blocking system routines.

## -see-also

