---
UID: NE:mfidl._MF_QUALITY_LEVEL
title: MF_QUALITY_LEVEL (mfidl.h)
description: Specifies the quality level for a pipeline component.
helpviewer_keywords: ["6fe5abbb-c079-4d74-9c75-6fb502054546","MF_NUM_QUALITY_LEVELS","MF_QUALITY_LEVEL","MF_QUALITY_LEVEL enumeration [Media Foundation]","MF_QUALITY_NORMAL","MF_QUALITY_NORMAL_MINUS_1","MF_QUALITY_NORMAL_MINUS_2","MF_QUALITY_NORMAL_MINUS_3","MF_QUALITY_NORMAL_MINUS_4","MF_QUALITY_NORMAL_MINUS_5","mf.mf_quality_level","mfidl/MF_NUM_QUALITY_LEVELS","mfidl/MF_QUALITY_LEVEL","mfidl/MF_QUALITY_NORMAL","mfidl/MF_QUALITY_NORMAL_MINUS_1","mfidl/MF_QUALITY_NORMAL_MINUS_2","mfidl/MF_QUALITY_NORMAL_MINUS_3","mfidl/MF_QUALITY_NORMAL_MINUS_4","mfidl/MF_QUALITY_NORMAL_MINUS_5"]
old-location: mf\mf_quality_level.htm
tech.root: mf
ms.assetid: 6fe5abbb-c079-4d74-9c75-6fb502054546
ms.date: 12/05/2018
ms.keywords: 6fe5abbb-c079-4d74-9c75-6fb502054546, MF_NUM_QUALITY_LEVELS, MF_QUALITY_LEVEL, MF_QUALITY_LEVEL enumeration [Media Foundation], MF_QUALITY_NORMAL, MF_QUALITY_NORMAL_MINUS_1, MF_QUALITY_NORMAL_MINUS_2, MF_QUALITY_NORMAL_MINUS_3, MF_QUALITY_NORMAL_MINUS_4, MF_QUALITY_NORMAL_MINUS_5, mf.mf_quality_level, mfidl/MF_NUM_QUALITY_LEVELS, mfidl/MF_QUALITY_LEVEL, mfidl/MF_QUALITY_NORMAL, mfidl/MF_QUALITY_NORMAL_MINUS_1, mfidl/MF_QUALITY_NORMAL_MINUS_2, mfidl/MF_QUALITY_NORMAL_MINUS_3, mfidl/MF_QUALITY_NORMAL_MINUS_4, mfidl/MF_QUALITY_NORMAL_MINUS_5
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: MF_QUALITY_LEVEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MF_QUALITY_LEVEL
 - mfidl/_MF_QUALITY_LEVEL
 - MF_QUALITY_LEVEL
 - mfidl/MF_QUALITY_LEVEL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MF_QUALITY_LEVEL
---

# MF_QUALITY_LEVEL enumeration


## -description

Specifies the quality level for a pipeline component. The quality level determines how the component consumes or produces samples.

## -enum-fields

### -field MF_QUALITY_NORMAL:0

Normal quality.

### -field MF_QUALITY_NORMAL_MINUS_1:0x1

One level below normal quality.

### -field MF_QUALITY_NORMAL_MINUS_2:0x2

Two levels below normal quality.

### -field MF_QUALITY_NORMAL_MINUS_3:0x3

Three levels below normal quality.

### -field MF_QUALITY_NORMAL_MINUS_4:0x4

Four levels below normal quality.

### -field MF_QUALITY_NORMAL_MINUS_5:0x5

Five levels below normal quality.

### -field MF_NUM_QUALITY_LEVELS:0x6

Maximum number of quality levels. This value is not a valid flag.

## -remarks

Each successive quality level decreases the amount of processing that is needed, while also reducing the resulting quality of the audio or video. The specific algorithm used to reduce quality depends on the component. Mode 1 is the least aggressive mode, and mode 5 is the most aggressive. A component is not required to implement all five levels. Also, the same quality level might not be comparable between two different components.
      

Video decoders can often reduce quality by leaving out certain post-processing steps. The enhanced video renderer (EVR) can sometimes reduce quality by switching to a different deinterlacing mode.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise">IMFQualityAdvise</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
