---
UID: NE:uxtheme._BP_BUFFERFORMAT
title: BP_BUFFERFORMAT (uxtheme.h)
description: Specifies the format of the buffer. Used by BeginBufferedAnimation and BeginBufferedPaint.
helpviewer_keywords: ["BPBF_COMPATIBLEBITMAP","BPBF_DIB","BPBF_TOPDOWNDIB","BPBF_TOPDOWNMONODIB","BP_BUFFERFORMAT","BP_BUFFERFORMAT enumeration [Windows Controls]","_shell_BP_BUFFERFORMAT","_shell_BP_BUFFERFORMAT_cpp","controls.BP_BUFFERFORMAT","controls._shell_BP_BUFFERFORMAT","uxtheme/BPBF_COMPATIBLEBITMAP","uxtheme/BPBF_DIB","uxtheme/BPBF_TOPDOWNDIB","uxtheme/BPBF_TOPDOWNMONODIB","uxtheme/BP_BUFFERFORMAT"]
old-location: controls\BP_BUFFERFORMAT.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\enums\bp_bufferformat.htm
ms.date: 12/05/2018
ms.keywords: BPBF_COMPATIBLEBITMAP, BPBF_DIB, BPBF_TOPDOWNDIB, BPBF_TOPDOWNMONODIB, BP_BUFFERFORMAT, BP_BUFFERFORMAT enumeration [Windows Controls], _shell_BP_BUFFERFORMAT, _shell_BP_BUFFERFORMAT_cpp, controls.BP_BUFFERFORMAT, controls._shell_BP_BUFFERFORMAT, uxtheme/BPBF_COMPATIBLEBITMAP, uxtheme/BPBF_DIB, uxtheme/BPBF_TOPDOWNDIB, uxtheme/BPBF_TOPDOWNMONODIB, uxtheme/BP_BUFFERFORMAT
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: BP_BUFFERFORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BP_BUFFERFORMAT
 - uxtheme/_BP_BUFFERFORMAT
 - BP_BUFFERFORMAT
 - uxtheme/BP_BUFFERFORMAT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Uxtheme.h
api_name:
 - BP_BUFFERFORMAT
---

# BP_BUFFERFORMAT enumeration


## -description

Specifies the format of the buffer. Used by <a href="/windows/desktop/api/uxtheme/nf-uxtheme-beginbufferedanimation">BeginBufferedAnimation</a> and <a href="/windows/desktop/api/uxtheme/nf-uxtheme-beginbufferedpaint">BeginBufferedPaint</a>.

## -enum-fields

### -field BPBF_COMPATIBLEBITMAP

Compatible bitmap. The  number of bits per pixel is based on the color format of the device associated with the HDC specified with <a href="/windows/desktop/api/uxtheme/nf-uxtheme-beginbufferedpaint">BeginBufferedPaint</a> or <a href="/windows/desktop/api/uxtheme/nf-uxtheme-beginbufferedanimation">BeginBufferedAnimation</a>—typically, this is the display device.

### -field BPBF_DIB

Bottom-up device-independent bitmap. The origin of the bitmap is the lower-left corner. Uses 32 bits per pixel.

### -field BPBF_TOPDOWNDIB

Top-down device-independent bitmap. The origin of the bitmap is the upper-left corner. Uses 32 bits per pixel.

### -field BPBF_TOPDOWNMONODIB

Top-down, monochrome, device-independent bitmap. Uses 1 bit per pixel.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap">CreateCompatibleBitmap</a>



<a href="/windows/desktop/gdi/device-independent-bitmaps">Device-Independent Bitmaps</a>



<b>Other Resources</b>