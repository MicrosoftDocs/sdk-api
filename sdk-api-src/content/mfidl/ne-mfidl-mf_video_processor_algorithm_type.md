---
UID: NE:mfidl._MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
title: MF_VIDEO_PROCESSOR_ALGORITHM_TYPE (mfidl.h)
description: Defines algorithms for the video processor which is use by MF_VIDEO_PROCESSOR_ALGORITHM.
helpviewer_keywords: ["MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT","MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444","MF_VIDEO_PROCESSOR_ALGORITHM_TYPE","MF_VIDEO_PROCESSOR_ALGORITHM_TYPE enumeration [Media Foundation]","mf.mf_video_processor_algorithm_type","mfidl/MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT","mfidl/MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444","mfidl/MF_VIDEO_PROCESSOR_ALGORITHM_TYPE"]
old-location: mf\mf_video_processor_algorithm_type.htm
tech.root: mf
ms.assetid: 3BB0836E-39E6-40FA-9BA0-C986EB587CF1
ms.date: 12/05/2018
ms.keywords: MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT, MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444, MF_VIDEO_PROCESSOR_ALGORITHM_TYPE, MF_VIDEO_PROCESSOR_ALGORITHM_TYPE enumeration [Media Foundation], mf.mf_video_processor_algorithm_type, mfidl/MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT, mfidl/MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444, mfidl/MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
 - mfidl/_MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
 - MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
 - mfidl/MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
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
 - MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
---

# MF_VIDEO_PROCESSOR_ALGORITHM_TYPE enumeration


## -description

Defines algorithms for the video processor which is use by <a href="/windows/desktop/medfound/mf-video-processor-algorithm">MF_VIDEO_PROCESSOR_ALGORITHM</a>.

## -enum-fields

### -field MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT:0

default mode favors a balance of quality and speed

### -field MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444:1

The video processor will always internally process in AYUV and use high quality filters.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
