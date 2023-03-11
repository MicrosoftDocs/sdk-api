---
UID: NE:d2d1effectauthor.D2D1_CHANNEL_DEPTH
title: D2D1_CHANNEL_DEPTH (d2d1effectauthor.h)
description: Allows a caller to control the channel depth of a stage in the rendering pipeline.
helpviewer_keywords: ["D2D1_CHANNEL_DEPTH","D2D1_CHANNEL_DEPTH enumeration [Direct2D]","D2D1_CHANNEL_DEPTH_1","D2D1_CHANNEL_DEPTH_4","D2D1_CHANNEL_DEPTH_DEFAULT","d2d1effectauthor/D2D1_CHANNEL_DEPTH","d2d1effectauthor/D2D1_CHANNEL_DEPTH_1","d2d1effectauthor/D2D1_CHANNEL_DEPTH_4","d2d1effectauthor/D2D1_CHANNEL_DEPTH_DEFAULT","direct2d.d2d1_channel_depth"]
old-location: direct2d\d2d1_channel_depth.htm
tech.root: Direct2D
ms.assetid: 78129b15-a770-49c0-b58b-8cb850f80006
ms.date: 12/05/2018
ms.keywords: D2D1_CHANNEL_DEPTH, D2D1_CHANNEL_DEPTH enumeration [Direct2D], D2D1_CHANNEL_DEPTH_1, D2D1_CHANNEL_DEPTH_4, D2D1_CHANNEL_DEPTH_DEFAULT, d2d1effectauthor/D2D1_CHANNEL_DEPTH, d2d1effectauthor/D2D1_CHANNEL_DEPTH_1, d2d1effectauthor/D2D1_CHANNEL_DEPTH_4, d2d1effectauthor/D2D1_CHANNEL_DEPTH_DEFAULT, direct2d.d2d1_channel_depth
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
req.type-library: D2d1effectauthor.lib
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_CHANNEL_DEPTH
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_CHANNEL_DEPTH
 - d2d1effectauthor/D2D1_CHANNEL_DEPTH
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - d2d1effectauthor.lib
api_name:
 - D2D1_CHANNEL_DEPTH
---

# D2D1_CHANNEL_DEPTH enumeration


## -description

Allows a caller to control the channel depth of a stage in the rendering pipeline.

## -enum-fields

### -field D2D1_CHANNEL_DEPTH_DEFAULT:0

The channel depth is the default. It is inherited from the inputs.

### -field D2D1_CHANNEL_DEPTH_1:1

The channel depth is 1.

### -field D2D1_CHANNEL_DEPTH_4:4

The channel depth is 4.

### -field D2D1_CHANNEL_DEPTH_FORCE_DWORD:0xffffffff

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1renderinfo-setoutputbuffer">ID2D1RenderInfo::SetOutputBuffer</a>
