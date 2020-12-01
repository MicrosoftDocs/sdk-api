---
UID: NE:vptype._AMVP_MODE
title: AMVP_MODE (vptype.h)
description: Specifies the various modes for video ports.
helpviewer_keywords: ["AMVP_MODE","AMVP_MODE","AMVP_MODE enumeration [DirectShow]","AMVP_MODEEnumeration","AMVP_MODE_BOBINTERLEAVED","AMVP_MODE_SKIPEVEN","AMVP_MODE_SKIPODD","AMVP_MODE_WEAVE","MODE_BOBNONINTERLEAVED","dshow.amvp_mode","vptype/AMVP_MODE","vptype/AMVP_MODE_BOBINTERLEAVED","vptype/AMVP_MODE_SKIPEVEN","vptype/AMVP_MODE_SKIPODD","vptype/AMVP_MODE_WEAVE","vptype/MODE_BOBNONINTERLEAVED"]
old-location: dshow\amvp_mode.htm
tech.root: dshow
ms.assetid: 73d63ca2-17fb-4e27-9ea5-62686117254a
ms.date: 12/05/2018
ms.keywords: AMVP_MODE, AMVP_MODE , AMVP_MODE enumeration [DirectShow], AMVP_MODEEnumeration, AMVP_MODE_BOBINTERLEAVED, AMVP_MODE_SKIPEVEN, AMVP_MODE_SKIPODD, AMVP_MODE_WEAVE, MODE_BOBNONINTERLEAVED, dshow.amvp_mode, vptype/AMVP_MODE, vptype/AMVP_MODE_BOBINTERLEAVED, vptype/AMVP_MODE_SKIPEVEN, vptype/AMVP_MODE_SKIPODD, vptype/AMVP_MODE_WEAVE, vptype/MODE_BOBNONINTERLEAVED
req.header: vptype.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: AMVP_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AMVP_MODE
 - vptype/_AMVP_MODE
 - AMVP_MODE
 - vptype/AMVP_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - vptype.h
api_name:
 - AMVP_MODE
---

# AMVP_MODE enumeration


## -description

Specifies the various modes for video ports.

## -enum-fields

### -field AMVP_MODE_WEAVE

Weave.

### -field AMVP_MODE_BOBINTERLEAVED

Interleaved bob. Bob mode in which resources are allocated to switch to weave mode, for example, on the next frame.

### -field AMVP_MODE_BOBNONINTERLEAVED

### -field AMVP_MODE_SKIPEVEN

Skip even fields.

### -field AMVP_MODE_SKIPODD

Skip odd fields.
          


#### - MODE_BOBNONINTERLEAVED

Noninterleaved bob. Bob mode in which resources are not allocated to switch to weave mode.

## -see-also

<b></b>



<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>