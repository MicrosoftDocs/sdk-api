---
UID: NS:mfmediaengine.MFVideoNormalizedRect
title: MFVideoNormalizedRect (mfmediaengine.h)
description: The MFVideoNormalizedRect (mfmediaengine.h) structure defines a normalized rectangle, which is used to specify sub-rectangles in a video rectangle.
helpviewer_keywords: ["MFVideoNormalizedRect","MFVideoNormalizedRect structure [Media Foundation]","c1dd42ca-64a0-4f30-82e1-eda3f4721526","evr/MFVideoNormalizedRect","mf.mfvideonormalizedrect"]
old-location: mf\mfvideonormalizedrect.htm
tech.root: mf
ms.assetid: c1dd42ca-64a0-4f30-82e1-eda3f4721526
ms.date: 08/05/2022
ms.keywords: MFVideoNormalizedRect, MFVideoNormalizedRect structure [Media Foundation], c1dd42ca-64a0-4f30-82e1-eda3f4721526, evr/MFVideoNormalizedRect, mf.mfvideonormalizedrect
req.header: mfmediaengine.h
req.include-header: Mfcaptureengine.h, Mfmediaengine.h
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
req.typenames: MFVideoNormalizedRect
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFVideoNormalizedRect
 - mfmediaengine/MFVideoNormalizedRect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - evr.h
api_name:
 - MFVideoNormalizedRect
---

# MFVideoNormalizedRect structure


## -description

Defines a normalized rectangle, which is used to specify sub-rectangles in a video rectangle. When a rectangle N is <i>normalized</i> relative to some other rectangle R, it means the following:

<ul>
<li>
The coordinate (0.0, 0.0) on N is mapped to the upper-left corner of R.

</li>
<li>
The coordinate (1.0, 1.0) on N is mapped to the lower-right corner of R.

</li>
</ul>
Any coordinates of N that fall outside the range [0...1] are mapped to positions outside the rectangle R. A normalized rectangle can be used to specify a region within a video rectangle without knowing the resolution or even the aspect ratio of the video. For example, the upper-left quadrant is defined as {0.0, 0.0, 0.5, 0.5}.

## -struct-fields

### -field left

X-coordinate of the upper-left corner of the rectangle.

### -field top

Y-coordinate of the upper-left corner of the rectangle.

### -field right

X-coordinate of the lower-right corner of the rectangle.

### -field bottom

Y-coordinate of the lower-right corner of the rectangle.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>
