---
UID: NS:wmsdkidl.tagWMVIDEOINFOHEADER2
title: WMVIDEOINFOHEADER2 (wmsdkidl.h)
description: The WMVIDEOINFOHEADER2 structure describes the bitmap and color information for a video image, including interlace, copy protection, and aspect ratio.
helpviewer_keywords: ["WMVIDEOINFOHEADER2","WMVIDEOINFOHEADER2 structure [windows Media Format]","wmformat.wmvideoinfoheader2","wmsdkidl/WMVIDEOINFOHEADER2"]
old-location: wmformat\wmvideoinfoheader2.htm
tech.root: wmformat
ms.assetid: 8da9d625-5cda-45bd-a664-7211593fab92
ms.date: 4/26/2023
ms.keywords: WMVIDEOINFOHEADER2, WMVIDEOINFOHEADER2 structure [windows Media Format], wmformat.wmvideoinfoheader2, wmsdkidl/WMVIDEOINFOHEADER2
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.typenames: WMVIDEOINFOHEADER2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWMVIDEOINFOHEADER2
 - wmsdkidl/tagWMVIDEOINFOHEADER2
 - WMVIDEOINFOHEADER2
 - wmsdkidl/WMVIDEOINFOHEADER2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WMVIDEOINFOHEADER2
---

# WMVIDEOINFOHEADER2 structure


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WMVIDEOINFOHEADER2</b> structure describes the bitmap and color information for a video image, including <a href="/windows/desktop/wmformat/wmformat-glossary">interlace</a>, copy protection, and aspect ratio.

## -struct-fields

### -field rcSource

<b>RECT</b> structure that specifies what part of the source stream should be used to fill the destination buffer. Renderers can use this field to ask the decoders to stretch or clip.

### -field rcTarget

<b>RECT</b> structure that specifies that specifies what part of the destination buffer should be used

### -field dwBitRate

Approximate data rate of the video stream, in bits per second.

### -field dwBitErrorRate

Data error rate of the video stream, in bits per second.

### -field AvgTimePerFrame

The video frame's average display time, in 100-nanosecond units.

### -field dwInterlaceFlags

Bit-wise combination of zero or more flags that describe interlacing behavior. The flags are defined in Dvdmedia.h in the DirectX SDK. Undefined bits must be set to zero or else the connection will be rejected.

### -field dwCopyProtectFlags

Flag set with the AMCOPYPROTECT_RestrictDuplication value (0x00000001) to indicate that the duplication of the stream should be restricted. Undefined bits must be set to zero or else the connection will be rejected.

### -field dwPictAspectRatioX

The X dimension of the video rectangle's aspect ratio. For example, 16 for a 16:9 rectangle.

### -field dwPictAspectRatioY

The Y dimension of the video rectangle's aspect ratio. For example, 9 for a 16:9 rectangle.

### -field dwReserved1

Reserved for future use. Must be zero. (Note: this is different from the corresponding member of the <b>VIDEOINFOHEADER2</b> structure used in DirectShow.

### -field dwReserved2

Reserved for future use. Must be zero.

### -field bmiHeader

<b>BITMAPINFOHEADER</b> structure that contains color and dimension information for the video image bitmap.

## -remarks

This structure is identical to the <b>VIDEOINFOHEADER2</b> structure defined in Dvdmedia.h. For more information, see the DirectShow documentation in the DirectX SDK.

## -see-also

<a href="/windows/desktop/wmformat/structures">Structures</a>