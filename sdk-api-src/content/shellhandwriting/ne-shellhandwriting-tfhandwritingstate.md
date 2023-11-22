---
UID: NE:shellhandwriting.TfHandwritingState
tech.root: input_ink
title: TfHandwritingState enumeration (shellhandwriting.h)
ms.date: 11/13/2023
targetos: Windows
description: Specifies how handwriting is handled by the system.
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
 - TfHandwritingState
f1_keywords:
 - TfHandwritingState
 - shellhandwriting/TfHandwritingState
dev_langs:
 - c++
helpviewer_keywords:
 - TfHandwritingState
---

# TfHandwritingState enumeration

## -description

Specifies how handwriting is processed by the system.

## -enum-fields

### -field TF_HANDWRITING_AUTO

Handwriting behavior is automatically configured based on the presence of a pen and the current handwriting user settings.

### -field TF_HANDWRITING_DISABLED

Handwriting behavior is disabled by the [Text Services Framework](/windows/win32/tsf/text-services-framework) (TSF) client.

### -field TF_HANDWRITING_ENABLED

Handwriting behavior is enabled by the TSF client (pen input is withheld from the client).

### -field TF_HANDWRITING_POINTERDELIVERY

Handwriting behavior is enabled by the TSF client (pen input is not withheld from the client), which is responsible for analyzing the pen input and handling buffering, intent determination, and target determination.

## -remarks

## -see-also

[GetHandwritingState method](nf-shellhandwriting-itfhandwriting-gethandwritingstate.md), [SetHandwritingState method](nf-shellhandwriting-itfhandwriting-sethandwritingstate.md)
