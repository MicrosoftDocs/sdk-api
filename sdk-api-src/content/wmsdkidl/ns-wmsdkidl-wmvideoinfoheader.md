---
UID: NS:wmsdkidl.tagWMVIDEOINFOHEADER
title: WMVIDEOINFOHEADER (wmsdkidl.h)
description: The WMVIDEOINFOHEADER structure describes the bitmap and color information for a video image.
helpviewer_keywords: ["WMVIDEOINFOHEADER","WMVIDEOINFOHEADER structure [windows Media Format]","wmformat.wmvideoinfoheader","wmsdkidl/WMVIDEOINFOHEADER"]
old-location: wmformat\wmvideoinfoheader.htm
tech.root: wmformat
ms.assetid: cf079efd-1759-4787-8aeb-85543847ac44
ms.date: 4/26/2023
ms.keywords: WMVIDEOINFOHEADER, WMVIDEOINFOHEADER structure [windows Media Format], wmformat.wmvideoinfoheader, wmsdkidl/WMVIDEOINFOHEADER
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
req.typenames: WMVIDEOINFOHEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWMVIDEOINFOHEADER
 - wmsdkidl/tagWMVIDEOINFOHEADER
 - WMVIDEOINFOHEADER
 - wmsdkidl/WMVIDEOINFOHEADER
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
 - WMVIDEOINFOHEADER
---

# WMVIDEOINFOHEADER structure


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WMVIDEOINFOHEADER</b> structure describes the bitmap and color information for a video image.

## -struct-fields

### -field rcSource

<b>RECT</b> structure that specifies the source video window.

### -field rcTarget

<b>RECT</b> structure that specifies the destination video window.

### -field dwBitRate

<b>DWORD</b> containing the approximate bit rate, in bits per second.

### -field dwBitErrorRate

<b>DWORD</b> containing the error rate for this stream, in bits per second.

### -field AvgTimePerFrame

When writing an ASF file, this member specifies the desired average time per frame in 100-nanosecond units. When reading an ASF file, this member is always zero.

### -field bmiHeader

<b>BITMAPINFOHEADER</b> structure that contains color and dimension information for the video image bitmap. <b>BITMAPINFOHEADER</b> is a Windows GDI structure.

## -remarks

This structure is identical to the DirectShow <b>VIDEOINFOHEADER</b> structure.

For uncompressed video of 16 or fewer bits per pixel (bpp), additional information is required. You must specify bit fields for 16 bpp and palette information for 8 or fewer bpp video. To convey this information, allocate enough consecutive memory to hold the additional information and copy the data to the memory directly following this structure. When you specify the address and size of this structure in the <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type">WM_MEDIA_TYPE</a> structure for a stream, include the size of the palette or bit field data.