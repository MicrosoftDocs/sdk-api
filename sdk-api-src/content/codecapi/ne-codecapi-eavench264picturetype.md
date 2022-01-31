---
UID: NE:codecapi.eAVEncH264PictureType
title: eAVEncH264PictureType (codecapi.h)
description: Specifies the type of picture that is output by a video encoder.
helpviewer_keywords: ["codecapi/eAVEncH264PictureType","codecapi/eAVEncH264PictureType_B","codecapi/eAVEncH264PictureType_IDR","codecapi/eAVEncH264PictureType_P","eAVEncH264PictureType","eAVEncH264PictureType enumeration [Media Foundation]","eAVEncH264PictureType_B","eAVEncH264PictureType_IDR","eAVEncH264PictureType_P","mf.eavench264picturetype"]
old-location: mf\eavench264picturetype.htm
tech.root: mf
ms.assetid: D73E2F87-EED3-4655-BB39-EB4C8E0B0058
ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncH264PictureType, codecapi/eAVEncH264PictureType_B, codecapi/eAVEncH264PictureType_IDR, codecapi/eAVEncH264PictureType_P, eAVEncH264PictureType, eAVEncH264PictureType enumeration [Media Foundation], eAVEncH264PictureType_B, eAVEncH264PictureType_IDR, eAVEncH264PictureType_P, mf.eavench264picturetype
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - eAVEncH264PictureType
 - codecapi/eAVEncH264PictureType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - codecapi.h
api_name:
 - eAVEncH264PictureType
---

# eAVEncH264PictureType enumeration


## -description

Specifies the type of picture that is output by a video encoder.

## -enum-fields

### -field eAVEncH264PictureType_IDR:0

Instantaneous decoding refresh (IDR) picture.

### -field eAVEncH264PictureType_P

Predictive (B) picture.

### -field eAVEncH264PictureType_B

Bi-predictive (B) picture.

## -remarks

This enumeration is used with the <a href="/windows/desktop/medfound/mfsampleextension-videoencodepicturetype">MFSampleExtension_VideoEncodePictureType</a> sample attribute.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
