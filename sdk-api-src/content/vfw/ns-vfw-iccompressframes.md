---
UID: NS:vfw.ICCOMPRESSFRAMES
title: ICCOMPRESSFRAMES (vfw.h)
description: The ICCOMPRESSFRAMES structure contains compression parameters used with the ICM_COMPRESS_FRAMES_INFO message.
helpviewer_keywords: ["ICCOMPRESSFRAMES","ICCOMPRESSFRAMES structure [Windows Multimedia]","_win32_ICCOMPRESSFRAMES_str","multimedia.iccompressframes","vfw/ICCOMPRESSFRAMES"]
old-location: multimedia\iccompressframes.htm
tech.root: Multimedia
ms.assetid: ced9ceea-d3fa-4496-886a-837545a28194
ms.date: 12/05/2018
ms.keywords: ICCOMPRESSFRAMES, ICCOMPRESSFRAMES structure [Windows Multimedia], _win32_ICCOMPRESSFRAMES_str, multimedia.iccompressframes, vfw/ICCOMPRESSFRAMES
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
req.typenames: ICCOMPRESSFRAMES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICCOMPRESSFRAMES
 - vfw/ICCOMPRESSFRAMES
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
 - ICCOMPRESSFRAMES
---

# ICCOMPRESSFRAMES structure


## -description

The <b>ICCOMPRESSFRAMES</b> structure contains compression parameters used with the <a href="/windows/desktop/Multimedia/icm-compress-frames-info">ICM_COMPRESS_FRAMES_INFO</a> message.

## -struct-fields

### -field dwFlags

Applicable flags. The following value is defined: <b>ICCOMPRESSFRAMES_PADDING</b>. If this value is used, padding is used with the frame.

### -field lpbiOutput

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure containing the output format.

### -field lOutput

Reserved; do not use.

### -field lpbiInput

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure containing the input format.

### -field lInput

Reserved; do not use.

### -field lStartFrame

Number of the first frame to compress.

### -field lFrameCount

Number of frames to compress.

### -field lQuality

Quality setting.

### -field lDataRate

Maximum data rate, in bytes per second.

### -field lKeyRate

Maximum number of frames between consecutive key frames.

### -field dwRate

Compression rate in an integer format. To obtain the rate in frames per second, divide this value by the value in <b>dwScale</b>.

### -field dwScale

Value used to scale <b>dwRate</b> to frames per second.

### -field dwOverheadPerFrame

Reserved; do not use.

### -field dwReserved2

Reserved; do not use.

### -field GetData

Reserved; do not use.

### -field PutData

Reserved; do not use.

## -see-also

<a href="/previous-versions//ms532290(v=vs.85)">BITMAPINFOHEADER</a>



<a href="/windows/desktop/Multimedia/icm-compress-frames-info">ICM_COMPRESS_FRAMES_INFO</a>



Video Compression Manager



<a href="/windows/desktop/Multimedia/video-compression-structures">Video Compression Structures</a>

