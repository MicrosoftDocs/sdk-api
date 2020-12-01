---
UID: NS:winddi._BLENDOBJ
title: BLENDOBJ (winddi.h)
description: The BLENDOBJ structure controls blending by specifying the blending functions for source and destination bitmaps.
helpviewer_keywords: ["*PBLENDOBJ","BLENDOBJ","BLENDOBJ structure [Display Devices]","PBLENDOBJ","PBLENDOBJ structure pointer [Display Devices]","display.blendobj","grstrcts_0d4470ae-12b0-41f4-8209-49b346e4829d.xml","winddi/BLENDOBJ","winddi/PBLENDOBJ"]
old-location: display\blendobj.htm
tech.root: display
ms.assetid: 1bbe5cb6-8722-45bb-ae43-01bc4460f08d
ms.date: 12/05/2018
ms.keywords: '*PBLENDOBJ, BLENDOBJ, BLENDOBJ structure [Display Devices], PBLENDOBJ, PBLENDOBJ structure pointer [Display Devices], display.blendobj, grstrcts_0d4470ae-12b0-41f4-8209-49b346e4829d.xml, winddi/BLENDOBJ, winddi/PBLENDOBJ'
req.header: winddi.h
req.include-header: Winddi.h
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
req.typenames: BLENDOBJ, *PBLENDOBJ
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BLENDOBJ
 - winddi/_BLENDOBJ
 - PBLENDOBJ
 - winddi/PBLENDOBJ
 - BLENDOBJ
 - winddi/BLENDOBJ
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - BLENDOBJ
---

# BLENDOBJ structure


## -description

The BLENDOBJ structure controls blending by specifying the blending functions for source and destination bitmaps.

## -struct-fields

### -field BlendFunction

Is a BLENDFUNCTION structure (described in the Microsoft Window SDK documentation) that specifies the blending operation to use, the alpha transparency for the source bitmap, and the way the source and destination bitmaps are interpreted.

