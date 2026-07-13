---
UID: NE:mfidl._MF_QUALITY_DROP_MODE
title: MF_QUALITY_DROP_MODE (mfidl.h)
description: Specifies how aggressively a pipeline component should drop samples.
helpviewer_keywords: ["MF_DROP_MODE_1","MF_DROP_MODE_2","MF_DROP_MODE_3","MF_DROP_MODE_4","MF_DROP_MODE_5","MF_DROP_MODE_NONE","MF_NUM_DROP_MODES","MF_QUALITY_DROP_MODE","MF_QUALITY_DROP_MODE enumeration [Media Foundation]","e40751d2-9abf-4fe6-8829-9b1fbf4531e8","mf.mf_quality_drop_mode","mfidl/MF_DROP_MODE_1","mfidl/MF_DROP_MODE_2","mfidl/MF_DROP_MODE_3","mfidl/MF_DROP_MODE_4","mfidl/MF_DROP_MODE_5","mfidl/MF_DROP_MODE_NONE","mfidl/MF_NUM_DROP_MODES","mfidl/MF_QUALITY_DROP_MODE"]
old-location: mf\mf_quality_drop_mode.htm
tech.root: mf
ms.assetid: e40751d2-9abf-4fe6-8829-9b1fbf4531e8
ms.date: 12/05/2018
ms.keywords: MF_DROP_MODE_1, MF_DROP_MODE_2, MF_DROP_MODE_3, MF_DROP_MODE_4, MF_DROP_MODE_5, MF_DROP_MODE_NONE, MF_NUM_DROP_MODES, MF_QUALITY_DROP_MODE, MF_QUALITY_DROP_MODE enumeration [Media Foundation], e40751d2-9abf-4fe6-8829-9b1fbf4531e8, mf.mf_quality_drop_mode, mfidl/MF_DROP_MODE_1, mfidl/MF_DROP_MODE_2, mfidl/MF_DROP_MODE_3, mfidl/MF_DROP_MODE_4, mfidl/MF_DROP_MODE_5, mfidl/MF_DROP_MODE_NONE, mfidl/MF_NUM_DROP_MODES, mfidl/MF_QUALITY_DROP_MODE
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
req.typenames: MF_QUALITY_DROP_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MF_QUALITY_DROP_MODE
 - mfidl/_MF_QUALITY_DROP_MODE
 - MF_QUALITY_DROP_MODE
 - mfidl/MF_QUALITY_DROP_MODE
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
 - MF_QUALITY_DROP_MODE
---

# MF_QUALITY_DROP_MODE enumeration


## -description

Specifies how aggressively a pipeline component should drop samples.

## -enum-fields

### -field MF_DROP_MODE_NONE:0

Normal processing of samples. Drop mode is disabled.

### -field MF_DROP_MODE_1:0x1

First drop mode (least aggressive).

### -field MF_DROP_MODE_2:0x2

Second drop mode.

### -field MF_DROP_MODE_3:0x3

Third drop mode.

### -field MF_DROP_MODE_4:0x4

Fourth drop mode.

### -field MF_DROP_MODE_5:0x5

Fifth drop mode (most aggressive, if it is supported; see Remarks).

### -field MF_NUM_DROP_MODES:0x6

Maximum number of drop modes. This value is not a valid flag.

## -remarks

In drop mode, a component drops samples, more or less aggressively depending on the level of the drop mode. The specific algorithm used depends on the component. Mode 1 is the least aggressive mode, and mode 5 is the most aggressive. A component is not required to implement all five levels.

For example, suppose an encoded video stream has three B-frames between each pair of P-frames. A decoder might implement the following drop modes:

<ul>
<li>
Mode 1: Drop one out of every three B frames.

</li>
<li>
Mode 2: Drop one out of every two B frames.

</li>
<li>
Mode 3: Drop all delta frames.

</li>
<li>
Modes 4 and 5: Unsupported.

</li>
</ul>
The enhanced video renderer (EVR) can drop video frames before sending them to the EVR mixer.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise">IMFQualityAdvise</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
