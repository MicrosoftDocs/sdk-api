---
UID: NS:vmr9._VMR9NormalizedRect
title: VMR9NormalizedRect (vmr9.h)
description: The VMR9NormalizedRect structure is used with the VMR-9 filter in mixing operations to specify or retrieve the location of a video rectangle in composition space.
helpviewer_keywords: ["VMR9NormalizedRect","VMR9NormalizedRect structure [DirectShow]","VMR9NormalizedRectStructure","dshow.vmr9normalizedrect","vmr9/VMR9NormalizedRect"]
old-location: dshow\vmr9normalizedrect.htm
tech.root: dshow
ms.assetid: 226b685c-92da-45c3-b99a-6c1e732f8dc6
ms.date: 12/05/2018
ms.keywords: VMR9NormalizedRect, VMR9NormalizedRect structure [DirectShow], VMR9NormalizedRectStructure, dshow.vmr9normalizedrect, vmr9/VMR9NormalizedRect
req.header: vmr9.h
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
req.typenames: VMR9NormalizedRect
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VMR9NormalizedRect
 - vmr9/_VMR9NormalizedRect
 - VMR9NormalizedRect
 - vmr9/VMR9NormalizedRect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vmr9.h
api_name:
 - VMR9NormalizedRect
---

# VMR9NormalizedRect structure


## -description

The <code>VMR9NormalizedRect</code> structure is used with the VMR-9 filter in mixing operations to specify or retrieve the location of a video rectangle in composition space.

## -struct-fields

### -field left

Specifies left.

### -field top

Specifies top.

### -field right

Specifies right.

### -field bottom

Specifies bottom.

## -remarks

This structure is used in methods involving "composition space," which refers to the visible video rectangle, as well as the "offscreen" space necessary to contain rectangles from secondary streams. See <a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a> for more information.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>