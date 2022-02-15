---
UID: NE:mfapi._MFVideoSrcContentHintFlags
title: MFVideoSrcContentHintFlags (mfapi.h)
description: Describes the intended aspect ratio for a video stream.
helpviewer_keywords: ["6166b880-36bc-4ac3-9d66-d3dd17c29ae7","MFVideoSrcContentHintFlag_16x9","MFVideoSrcContentHintFlag_235_1","MFVideoSrcContentHintFlag_None","MFVideoSrcContentHintFlags","MFVideoSrcContentHintFlags enumeration [Media Foundation]","mf.mfvideosrccontenthintflags","mfapi/MFVideoSrcContentHintFlag_16x9","mfapi/MFVideoSrcContentHintFlag_235_1","mfapi/MFVideoSrcContentHintFlag_None","mfapi/MFVideoSrcContentHintFlags"]
old-location: mf\mfvideosrccontenthintflags.htm
tech.root: mf
ms.assetid: 6166b880-36bc-4ac3-9d66-d3dd17c29ae7
ms.date: 12/05/2018
ms.keywords: 6166b880-36bc-4ac3-9d66-d3dd17c29ae7, MFVideoSrcContentHintFlag_16x9, MFVideoSrcContentHintFlag_235_1, MFVideoSrcContentHintFlag_None, MFVideoSrcContentHintFlags, MFVideoSrcContentHintFlags enumeration [Media Foundation], mf.mfvideosrccontenthintflags, mfapi/MFVideoSrcContentHintFlag_16x9, mfapi/MFVideoSrcContentHintFlag_235_1, mfapi/MFVideoSrcContentHintFlag_None, mfapi/MFVideoSrcContentHintFlags
req.header: mfapi.h
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
req.typenames: MFVideoSrcContentHintFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFVideoSrcContentHintFlags
 - mfapi/_MFVideoSrcContentHintFlags
 - MFVideoSrcContentHintFlags
 - mfapi/MFVideoSrcContentHintFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - MFVideoSrcContentHintFlags
---

# MFVideoSrcContentHintFlags enumeration


## -description

Describes the intended aspect ratio for a video stream.

## -enum-fields

### -field MFVideoSrcContentHintFlag_None:0

The aspect ratio is unknown.

### -field MFVideoSrcContentHintFlag_16x9:1

The source is 16×9 content encoded within a 4×3 area.

### -field MFVideoSrcContentHintFlag_235_1:2

The source is 2.35:1 content encoded within a 16×9 or 4×3 area.

## -remarks

Use these flags with the <a href="/windows/desktop/medfound/mf-mt-source-content-hint-attribute">MF_MT_SOURCE_CONTENT_HINT</a> attribute.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
