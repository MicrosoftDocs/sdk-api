---
UID: NE:d2d1effectauthor.D2D1_VERTEX_OPTIONS
title: D2D1_VERTEX_OPTIONS (d2d1effectauthor.h)
description: Describes flags that influence how the renderer interacts with a custom vertex shader.
helpviewer_keywords: ["D2D1_VERTEX_OPTIONS","D2D1_VERTEX_OPTIONS enumeration [Direct2D]","D2D1_VERTEX_OPTIONS_ASSUME_NO_OVERLAP","D2D1_VERTEX_OPTIONS_DO_NOT_CLEAR","D2D1_VERTEX_OPTIONS_NONE","D2D1_VERTEX_OPTIONS_USE_DEPTH_BUFFER","d2d1effectauthor/D2D1_VERTEX_OPTIONS","d2d1effectauthor/D2D1_VERTEX_OPTIONS_ASSUME_NO_OVERLAP","d2d1effectauthor/D2D1_VERTEX_OPTIONS_DO_NOT_CLEAR","d2d1effectauthor/D2D1_VERTEX_OPTIONS_NONE","d2d1effectauthor/D2D1_VERTEX_OPTIONS_USE_DEPTH_BUFFER","direct2d.d2d1_vertex_options"]
old-location: direct2d\d2d1_vertex_options.htm
tech.root: Direct2D
ms.assetid: b308aaf4-edf0-49a8-8fbf-04bb38c00605
ms.date: 12/05/2018
ms.keywords: D2D1_VERTEX_OPTIONS, D2D1_VERTEX_OPTIONS enumeration [Direct2D], D2D1_VERTEX_OPTIONS_ASSUME_NO_OVERLAP, D2D1_VERTEX_OPTIONS_DO_NOT_CLEAR, D2D1_VERTEX_OPTIONS_NONE, D2D1_VERTEX_OPTIONS_USE_DEPTH_BUFFER, d2d1effectauthor/D2D1_VERTEX_OPTIONS, d2d1effectauthor/D2D1_VERTEX_OPTIONS_ASSUME_NO_OVERLAP, d2d1effectauthor/D2D1_VERTEX_OPTIONS_DO_NOT_CLEAR, d2d1effectauthor/D2D1_VERTEX_OPTIONS_NONE, d2d1effectauthor/D2D1_VERTEX_OPTIONS_USE_DEPTH_BUFFER, direct2d.d2d1_vertex_options
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: D2d1.lib; D2d1.dll
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_VERTEX_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_VERTEX_OPTIONS
 - d2d1effectauthor/D2D1_VERTEX_OPTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2d1.lib
 - D2d1.dll
api_name:
 - D2D1_VERTEX_OPTIONS
---

# D2D1_VERTEX_OPTIONS enumeration


## -description

Describes flags that influence how the renderer interacts with a custom vertex shader.

## -enum-fields

### -field D2D1_VERTEX_OPTIONS_NONE:0

The logical equivalent of having no flags set.

### -field D2D1_VERTEX_OPTIONS_DO_NOT_CLEAR:1

If this flag is set, the renderer  assumes that the vertex shader will cover the entire region of interest with vertices and need not clear the destination render target. If this flag is not set, the renderer assumes that the vertices do not cover the entire region interest and must clear the render target to transparent black first.

### -field D2D1_VERTEX_OPTIONS_USE_DEPTH_BUFFER:2

The renderer will use a depth buffer when rendering custom vertices. The depth buffer will be used for calculating occlusion information. This can result in the renderer output being draw-order dependent if it contains transparency.

### -field D2D1_VERTEX_OPTIONS_ASSUME_NO_OVERLAP:4

Indicates that custom vertices do not overlap each other.

### -field D2D1_VERTEX_OPTIONS_FORCE_DWORD:0xffffffff

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description">D2D1_BLEND_DESCRIPTION</a>



<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1blendtransform">ID2D1BlendTransform</a>
