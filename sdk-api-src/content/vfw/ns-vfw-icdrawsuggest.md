---
UID: NS:vfw.ICDRAWSUGGEST
title: ICDRAWSUGGEST (vfw.h)
description: The ICDRAWSUGGEST structure contains compression parameters used with the ICM_DRAW_SUGGESTFORMAT message to suggest an appropriate input format.
helpviewer_keywords: ["ICDRAWSUGGEST","ICDRAWSUGGEST structure [Windows Multimedia]","_win32_ICDRAWSUGGEST_str","multimedia.icdrawsuggest","vfw/ICDRAWSUGGEST"]
old-location: multimedia\icdrawsuggest.htm
tech.root: Multimedia
ms.assetid: d8dab197-7364-4f90-b08e-c913df85723e
ms.date: 12/05/2018
ms.keywords: ICDRAWSUGGEST, ICDRAWSUGGEST structure [Windows Multimedia], _win32_ICDRAWSUGGEST_str, multimedia.icdrawsuggest, vfw/ICDRAWSUGGEST
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: ICDRAWSUGGEST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICDRAWSUGGEST
 - vfw/ICDRAWSUGGEST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - ICDRAWSUGGEST
---

# ICDRAWSUGGEST structure


## -description

The <b>ICDRAWSUGGEST</b> structure contains compression parameters used with the <a href="/windows/desktop/Multimedia/icm-draw-suggestformat">ICM_DRAW_SUGGESTFORMAT</a> message to suggest an appropriate input format.

## -struct-fields

### -field lpbiIn

Pointer to the structure containing the compressed input format.

### -field lpbiSuggest

Pointer to a buffer to return a compatible input format for the renderer.

### -field dxSrc

Width of the source rectangle.

### -field dySrc

Height of the source rectangle.

### -field dxDst

Width of the destination rectangle.

### -field dyDst

Height of the destination rectangle.

### -field hicDecompressor

Handle to a decompressor that supports the format of data described in <b>lpbiIn</b>.

## -see-also

<a href="/windows/desktop/Multimedia/icm-draw-suggestformat">ICM_DRAW_SUGGESTFORMAT</a>



Video Compression Manager



<a href="/windows/desktop/Multimedia/video-compression-structures">Video Compression Structures</a>

