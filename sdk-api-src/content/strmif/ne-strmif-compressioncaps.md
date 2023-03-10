---
UID: NE:strmif.CompressionCaps
title: CompressionCaps (strmif.h)
description: Indicates video compression capabilities.
helpviewer_keywords: ["CompressionCaps","CompressionCaps enumeration [DirectShow]","CompressionCapsEnumeration","CompressionCaps_CanBFrame","CompressionCaps_CanCrunch","CompressionCaps_CanKeyFrame","CompressionCaps_CanQuality","CompressionCaps_CanWindow","dshow.compressioncaps","strmif/CompressionCaps","strmif/CompressionCaps_CanBFrame","strmif/CompressionCaps_CanCrunch","strmif/CompressionCaps_CanKeyFrame","strmif/CompressionCaps_CanQuality","strmif/CompressionCaps_CanWindow"]
old-location: dshow\compressioncaps.htm
tech.root: dshow
ms.assetid: e964756f-1c60-42fd-8497-637d5fc005d7
ms.date: 12/05/2018
ms.keywords: CompressionCaps, CompressionCaps enumeration [DirectShow], CompressionCapsEnumeration, CompressionCaps_CanBFrame, CompressionCaps_CanCrunch, CompressionCaps_CanKeyFrame, CompressionCaps_CanQuality, CompressionCaps_CanWindow, dshow.compressioncaps, strmif/CompressionCaps, strmif/CompressionCaps_CanBFrame, strmif/CompressionCaps_CanCrunch, strmif/CompressionCaps_CanKeyFrame, strmif/CompressionCaps_CanQuality, strmif/CompressionCaps_CanWindow
req.header: strmif.h
req.include-header: Dshow.h
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
req.typenames: CompressionCaps
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CompressionCaps
 - strmif/CompressionCaps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - CompressionCaps
---

# CompressionCaps enumeration


## -description

Indicates video compression capabilities.

## -enum-fields

### -field CompressionCaps_CanQuality:0x1

Video compressor supports the <a href="/windows/desktop/api/strmif/nf-strmif-iamvideocompression-put_quality">IAMVideoCompression::put_Quality</a> and <a href="/windows/desktop/api/strmif/nf-strmif-iamvideocompression-get_quality">IAMVideoCompression::get_Quality</a> methods.

### -field CompressionCaps_CanCrunch:0x2

Video compressor can compress video to a specified data rate. If the compressor has this capability then the output pins media type will contain the data rate in the <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader">VIDEOINFOHEADER</a> structure's <b>dwBitRate</b> member. The only way to set the data rate is to set <b>dwBitRate</b>.

### -field CompressionCaps_CanKeyFrame:0x4

Video compressor supports the <a href="/windows/desktop/api/strmif/nf-strmif-iamvideocompression-put_keyframerate">IAMVideoCompression::put_KeyFrameRate</a> and <a href="/windows/desktop/api/strmif/nf-strmif-iamvideocompression-get_keyframerate">IAMVideoCompression::get_KeyFrameRate</a> methods.

### -field CompressionCaps_CanBFrame:0x8

Video compressor supports the <a href="/windows/desktop/api/strmif/nf-strmif-iamvideocompression-put_pframesperkeyframe">IAMVideoCompression::put_PFramesPerKeyFrame</a> and <a href="/windows/desktop/api/strmif/nf-strmif-iamvideocompression-get_pframesperkeyframe">IAMVideoCompression::get_PFramesPerKeyFrame</a> methods.

### -field CompressionCaps_CanWindow:0x10

Video compressor supports the <a href="/windows/desktop/api/strmif/nf-strmif-iamvideocompression-put_windowsize">IAMVideoCompression::put_WindowSize</a> and <a href="/windows/desktop/api/strmif/nf-strmif-iamvideocompression-get_windowsize">IAMVideoCompression::get_WindowSize</a> methods.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvideocompression">IAMVideoCompression Interface</a>
