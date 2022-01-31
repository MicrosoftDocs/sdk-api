---
UID: NE:wincodec.WICJpegIndexingOptions
title: WICJpegIndexingOptions (wincodec.h)
description: Specifies the options for indexing a JPEG image.
helpviewer_keywords: ["WICJpegIndexingOptions","WICJpegIndexingOptions enumeration [Windows Imaging Component]","WICJpegIndexingOptionsGenerateOnDemand","WICJpegIndexingOptionsGenerateOnLoad","WICJpegIndexingOptions_FORCE_DWORD","wic.wicjpegindexingoptions","wincodec/WICJpegIndexingOptions","wincodec/WICJpegIndexingOptionsGenerateOnDemand","wincodec/WICJpegIndexingOptionsGenerateOnLoad","wincodec/WICJpegIndexingOptions_FORCE_DWORD"]
old-location: wic\wicjpegindexingoptions.htm
tech.root: wic
ms.assetid: AFA9CC1B-847A-4237-9942-EC721FA86E4E
ms.date: 12/05/2018
ms.keywords: WICJpegIndexingOptions, WICJpegIndexingOptions enumeration [Windows Imaging Component], WICJpegIndexingOptionsGenerateOnDemand, WICJpegIndexingOptionsGenerateOnLoad, WICJpegIndexingOptions_FORCE_DWORD, wic.wicjpegindexingoptions, wincodec/WICJpegIndexingOptions, wincodec/WICJpegIndexingOptionsGenerateOnDemand, wincodec/WICJpegIndexingOptionsGenerateOnLoad, wincodec/WICJpegIndexingOptions_FORCE_DWORD
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
req.typenames: WICJpegIndexingOptions
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICJpegIndexingOptions
 - wincodec/WICJpegIndexingOptions
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
 - WICJpegIndexingOptions
---

# WICJpegIndexingOptions enumeration


## -description

Specifies the options for indexing a JPEG image.

## -enum-fields

### -field WICJpegIndexingOptionsGenerateOnDemand:0

Index generation is deferred until <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels">IWICBitmapSource::CopyPixels</a> is called on the image.

### -field WICJpegIndexingOptionsGenerateOnLoad:0x1

Index generation is performed when the when the image is initially loaded.

### -field WICJpegIndexingOptions_FORCE_DWORD:0x7fffffff

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used.

## -see-also

<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-setindexing">IWICJpegFrameDecode::SetIndexing</a>
