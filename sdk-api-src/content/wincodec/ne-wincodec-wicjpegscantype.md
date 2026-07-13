---
UID: NE:wincodec.WICJpegScanType
title: WICJpegScanType (wincodec.h)
description: Specifies the memory layout of pixel data in a JPEG image scan.
helpviewer_keywords: ["WICJpegScanType","WICJpegScanType enumeration [Windows Imaging Component]","WICJpegScanTypeInterleaved","WICJpegScanTypePlanarComponents","WICJpegScanTypeProgressive","WICJpegScanType_FORCE_DWORD","wic.wicjpegscantype","wincodec/WICJpegScanType","wincodec/WICJpegScanTypeInterleaved","wincodec/WICJpegScanTypePlanarComponents","wincodec/WICJpegScanTypeProgressive","wincodec/WICJpegScanType_FORCE_DWORD"]
old-location: wic\wicjpegscantype.htm
tech.root: wic
ms.assetid: DC8B42F0-66D3-4425-9AA8-6B8F0D9B8568
ms.date: 12/05/2018
ms.keywords: WICJpegScanType, WICJpegScanType enumeration [Windows Imaging Component], WICJpegScanTypeInterleaved, WICJpegScanTypePlanarComponents, WICJpegScanTypeProgressive, WICJpegScanType_FORCE_DWORD, wic.wicjpegscantype, wincodec/WICJpegScanType, wincodec/WICJpegScanTypeInterleaved, wincodec/WICJpegScanTypePlanarComponents, wincodec/WICJpegScanTypeProgressive, wincodec/WICJpegScanType_FORCE_DWORD
req.header: wincodec.h
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
req.typenames: WICJpegScanType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICJpegScanType
 - wincodec/WICJpegScanType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wincodec.h
api_name:
 - WICJpegScanType
---

# WICJpegScanType enumeration


## -description

Specifies the memory layout of pixel data in a JPEG image scan.

## -enum-fields

### -field WICJpegScanTypeInterleaved:0

The pixel data is stored in an interleaved memory layout.

### -field WICJpegScanTypePlanarComponents:0x1

The pixel data is stored in a planar memory layout.

### -field WICJpegScanTypeProgressive:0x2

The pixel data is stored in a progressive layout.

### -field WICJpegScanType_FORCE_DWORD:0x7fffffff

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used.

## -see-also

<a href="/windows/desktop/api/wincodec/ne-wincodec-wicjpegscantype">WICJpegScanType</a>
