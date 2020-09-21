---
UID: NF:amvideo.RESET_MASKS
title: RESET_MASKS macro (amvideo.h)
description: The RESET_MASKS macro fills the color mask fields in a VIDEOINFO structure with zeroes.
helpviewer_keywords: ["RESET_MASKS","RESET_MASKS macro [DirectShow]","amvideo/RESET_MASKS","dshow.reset_masks"]
old-location: dshow\reset_masks.htm
tech.root: dshow
ms.assetid: 039a43c1-c795-4374-ada8-2ea611c6409a
ms.date: 12/05/2018
ms.keywords: RESET_MASKS, RESET_MASKS macro [DirectShow], amvideo/RESET_MASKS, dshow.reset_masks
req.header: amvideo.h
req.include-header: Streams.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RESET_MASKS
 - amvideo/RESET_MASKS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Amvideo.h
api_name:
 - RESET_MASKS
---

# RESET_MASKS macro


## -description

The <b>RESET_MASKS</b> macro fills the color mask fields in a <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo">VIDEOINFO</a> structure with zeroes.

## -parameters

### -param pbmi

Pointer to a <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo">VIDEOINFO</a> structure.

## -remarks

As defined in the header file Amvideo.h, this macro is not correct and will cause a compile error. Replace it with the following:


```cpp

#undef RESET_MASKS
#define RESET_MASKS(x) (ZeroMemory((PVOID)(x)->dwBitMasks, SIZE_MASKS))

```

## -see-also

<a href="/windows/desktop/DirectShow/video-and-image-functions">Video and Image Functions</a>