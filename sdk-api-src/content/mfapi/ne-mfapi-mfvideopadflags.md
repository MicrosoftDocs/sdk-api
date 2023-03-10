---
UID: NE:mfapi._MFVideoPadFlags
title: MFVideoPadFlags (mfapi.h)
description: Specifies whether to pad a video image so that it fits within a specified aspect ratio.
helpviewer_keywords: ["MFVideoPadFlag_PAD_TO_16x9","MFVideoPadFlag_PAD_TO_4x3","MFVideoPadFlag_PAD_TO_None","MFVideoPadFlags","MFVideoPadFlags enumeration [Media Foundation]","c68fdd6e-4fc9-4d70-91f0-dab70315ec21","mf.mfvideopadflags","mfapi/MFVideoPadFlag_PAD_TO_16x9","mfapi/MFVideoPadFlag_PAD_TO_4x3","mfapi/MFVideoPadFlag_PAD_TO_None","mfapi/MFVideoPadFlags"]
old-location: mf\mfvideopadflags.htm
tech.root: mf
ms.assetid: c68fdd6e-4fc9-4d70-91f0-dab70315ec21
ms.date: 12/05/2018
ms.keywords: MFVideoPadFlag_PAD_TO_16x9, MFVideoPadFlag_PAD_TO_4x3, MFVideoPadFlag_PAD_TO_None, MFVideoPadFlags, MFVideoPadFlags enumeration [Media Foundation], c68fdd6e-4fc9-4d70-91f0-dab70315ec21, mf.mfvideopadflags, mfapi/MFVideoPadFlag_PAD_TO_16x9, mfapi/MFVideoPadFlag_PAD_TO_4x3, mfapi/MFVideoPadFlag_PAD_TO_None, mfapi/MFVideoPadFlags
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
req.typenames: MFVideoPadFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFVideoPadFlags
 - mfapi/_MFVideoPadFlags
 - MFVideoPadFlags
 - mfapi/MFVideoPadFlags
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
 - MFVideoPadFlags
---

# MFVideoPadFlags enumeration


## -description

Specifies whether to pad a video image so that it fits within a specified aspect ratio.

## -enum-fields

### -field MFVideoPadFlag_PAD_TO_None:0

Do not pad the image.

### -field MFVideoPadFlag_PAD_TO_4x3:1

Pad the image so that it can be displayed in a 4×3 area.

### -field MFVideoPadFlag_PAD_TO_16x9:2

Pad the image so that it can be displayed in a 16×9 area.

## -remarks

Use these flags with the <a href="/windows/desktop/medfound/mf-mt-pad-control-flags-attribute">MF_MT_PAD_CONTROL_FLAGS</a> attribute.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
