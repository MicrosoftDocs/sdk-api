---
UID: NS:dwrite.DWRITE_TEXT_METRICS
title: DWRITE_TEXT_METRICS (dwrite.h)
description: Contains the metrics associated with text after layout. (DWRITE_TEXT_METRICS)
helpviewer_keywords: ["DWRITE_TEXT_METRICS","DWRITE_TEXT_METRICS structure [Direct Write]","directwrite.dwrite_text_metrics","dwrite/DWRITE_TEXT_METRICS"]
old-location: directwrite\dwrite_text_metrics.htm
tech.root: DirectWrite
ms.assetid: 4524ace3-fca6-4daf-9ecb-516771e53fc9
ms.date: 12/05/2018
ms.keywords: DWRITE_TEXT_METRICS, DWRITE_TEXT_METRICS structure [Direct Write], directwrite.dwrite_text_metrics, dwrite/DWRITE_TEXT_METRICS
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DWRITE_TEXT_METRICS
 - dwrite/DWRITE_TEXT_METRICS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite.h
api_name:
 - DWRITE_TEXT_METRICS
---

# DWRITE_TEXT_METRICS structure


## -description

Contains the metrics associated with text after layout. 
  All coordinates are in device independent pixels (DIPs).

## -struct-fields

### -field left

Type: <b>FLOAT</b>

A value that indicates the left-most point of formatted text relative to the layout box, 
	  while excluding any glyph overhang.

### -field top

Type: <b>FLOAT</b>

A value that indicates the top-most point of formatted text relative to the layout box, while excluding any glyph overhang.

### -field width

Type: <b>FLOAT</b>

A value that indicates the width of the formatted text, while ignoring trailing whitespace 
	  at the end of each line.

### -field widthIncludingTrailingWhitespace

Type: <b>FLOAT</b>

The width of the formatted text, taking into account the 
	  trailing whitespace at the end of each line.

### -field height

Type: <b>FLOAT</b>

The height of the formatted text. The height of an empty string 
	  is set to the same value as that of the default font.

### -field layoutWidth

Type: <b>FLOAT</b>

The initial width given to the layout. It can be either larger or smaller than the 
	  text content width, depending on whether the text 
	  was wrapped.

### -field layoutHeight

Type: <b>FLOAT</b>

Initial height given to the layout. Depending on the length of the text, it may be larger or smaller than the text content height.

### -field maxBidiReorderingDepth

Type: <b>UINT32</b>

The maximum reordering count of any line of text, used 
	  to calculate the most number of hit-testing boxes needed. 
	  If the layout has no bidirectional text, or no text at all, 
	  the minimum level is 1.

### -field lineCount

Type: <b>UINT32</b>

Total number of lines.

