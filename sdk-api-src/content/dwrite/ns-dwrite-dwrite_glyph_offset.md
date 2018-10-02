---
UID: NS:dwrite.DWRITE_GLYPH_OFFSET
title: DWRITE_GLYPH_OFFSET
author: windows-sdk-content
description: The optional adjustment to a glyph's position.
old-location: directwrite\dwrite_glyph_offset.htm
tech.root: DirectWrite
ms.assetid: f5a231c0-78df-4fe0-99a8-81fcad517cda
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DWRITE_GLYPH_OFFSET, DWRITE_GLYPH_OFFSET structure [Direct Write], directwrite.dwrite_glyph_offset, dwrite/DWRITE_GLYPH_OFFSET
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dwrite.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite.h
api_name:
 - DWRITE_GLYPH_OFFSET
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DWRITE_GLYPH_OFFSET structure


## -description


The optional adjustment to a glyph's position.


## -struct-fields




### -field advanceOffset

Type: <b>FLOAT</b>

The offset in the advance direction of the run. A positive advance offset moves the glyph to the right (in pre-transform coordinates) if the run is left-to-right or to the left if the run is right-to-left.


### -field ascenderOffset

Type: <b>FLOAT</b>

The offset in the ascent direction, that is, the direction ascenders point. A positive ascender offset moves the glyph up (in pre-transform coordinates).  A negative ascender offset moves the glyph down.


## -remarks



An glyph offset changes the position of a glyph without affecting the pen position. Offsets are in logical, pre-transform units.



