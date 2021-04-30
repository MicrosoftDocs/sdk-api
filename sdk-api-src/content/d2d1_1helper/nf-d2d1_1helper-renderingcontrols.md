---
UID: NF:d2d1_1helper.RenderingControls
title: RenderingControls function (d2d1_1helper.h)
description: Returns a filled D2D1_RENDERING_CONTROLS structure.
helpviewer_keywords: ["RenderingControls","RenderingControls function [Direct2D]","d2d1_1helper/RenderingControls","direct2d.renderingcontrols"]
old-location: direct2d\renderingcontrols.htm
tech.root: Direct2D
ms.assetid: 5004EA84-216C-4758-8AA1-7E823583871E
ms.date: 12/05/2018
ms.keywords: RenderingControls, RenderingControls function [Direct2D], d2d1_1helper/RenderingControls, direct2d.renderingcontrols
req.header: d2d1_1helper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RenderingControls
 - d2d1_1helper/RenderingControls
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - RenderingControls
---

# RenderingControls function


## -description

Returns a filled D2D1_RENDERING_CONTROLS structure.

## -parameters

### -param bufferPrecision

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_buffer_precision">D2D1_BUFFER_PRECISION</a></b>

The buffer precision used by default if the buffer precision is not otherwise specified by the effect or the transform.

### -param tileSize

Type: <b><a href="/windows/desktop/Direct2D/d2d1-size-u">D2D1_SIZE_U</a></b>

The minimum tile allocation size to be used by the imaging effect renderer.

## -returns

Type: <b><a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_rendering_controls">D2D1_RENDERING_CONTROLS</a></b>

Describes limitations to be applied to an imaging effect renderer.