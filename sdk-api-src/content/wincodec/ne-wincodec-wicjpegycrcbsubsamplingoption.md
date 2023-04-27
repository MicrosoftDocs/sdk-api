---
UID: NE:wincodec.WICJpegYCrCbSubsamplingOption
title: WICJpegYCrCbSubsamplingOption (wincodec.h)
description: Specifies the JPEG YCrCB subsampling options.
helpviewer_keywords: ["WICJpegYCrCbSubsampling420","WICJpegYCrCbSubsampling422","WICJpegYCrCbSubsampling440","WICJpegYCrCbSubsampling444","WICJpegYCrCbSubsamplingDefault","WICJpegYCrCbSubsamplingOption","WICJpegYCrCbSubsamplingOption enumeration [Windows Imaging Component]","_wic_codec_wicjpegycrcbsubsamplingoption","wic._wic_codec_wicjpegycrcbsubsamplingoption","wincodec/WICJpegYCrCbSubsampling420","wincodec/WICJpegYCrCbSubsampling422","wincodec/WICJpegYCrCbSubsampling440","wincodec/WICJpegYCrCbSubsampling444","wincodec/WICJpegYCrCbSubsamplingDefault","wincodec/WICJpegYCrCbSubsamplingOption"]
old-location: wic\_wic_codec_wicjpegycrcbsubsamplingoption.htm
tech.root: wic
ms.assetid: 6ff16a79-35c9-4230-8f1c-a5c40aecc09e
ms.date: 12/05/2018
ms.keywords: WICJpegYCrCbSubsampling420, WICJpegYCrCbSubsampling422, WICJpegYCrCbSubsampling440, WICJpegYCrCbSubsampling444, WICJpegYCrCbSubsamplingDefault, WICJpegYCrCbSubsamplingOption, WICJpegYCrCbSubsamplingOption enumeration [Windows Imaging Component], _wic_codec_wicjpegycrcbsubsamplingoption, wic._wic_codec_wicjpegycrcbsubsamplingoption, wincodec/WICJpegYCrCbSubsampling420, wincodec/WICJpegYCrCbSubsampling422, wincodec/WICJpegYCrCbSubsampling440, wincodec/WICJpegYCrCbSubsampling444, wincodec/WICJpegYCrCbSubsamplingDefault, wincodec/WICJpegYCrCbSubsamplingOption
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WICJpegYCrCbSubsamplingOption
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICJpegYCrCbSubsamplingOption
 - wincodec/WICJpegYCrCbSubsamplingOption
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincodec.h
api_name:
 - WICJpegYCrCbSubsamplingOption
---

# WICJpegYCrCbSubsamplingOption enumeration


## -description

Specifies the JPEG YCrCB subsampling options.

## -enum-fields

### -field WICJpegYCrCbSubsamplingDefault:0

The default subsampling option.

### -field WICJpegYCrCbSubsampling420:0x1

Subsampling option that uses both horizontal and vertical decimation.

### -field WICJpegYCrCbSubsampling422:0x2

Subsampling option that uses horizontal decimation  .

### -field WICJpegYCrCbSubsampling444:0x3

Subsampling option that uses no decimation.

### -field WICJpegYCrCbSubsampling440:0x4

Subsampling option that uses 2x vertical downsampling only. This option is only available in Windows 8.1 and later.

### -field WICJPEGYCRCBSUBSAMPLING_FORCE_DWORD:0x7fffffff

## -remarks

The native JPEG encoder uses <b>WICJpegYCrCbSubsampling420</b>.

