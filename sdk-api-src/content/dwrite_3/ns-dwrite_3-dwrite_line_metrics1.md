---
UID: NS:dwrite_3.DWRITE_LINE_METRICS1
title: DWRITE_LINE_METRICS1 (dwrite_3.h)
description: Contains information about a formatted line of text. (DWRITE_LINE_METRICS1)
helpviewer_keywords: ["DWRITE_LINE_METRICS1","DWRITE_LINE_METRICS1 structure [Direct Write]","directwrite.dwrite_line_metrics1","dwrite_3/DWRITE_LINE_METRICS1"]
old-location: directwrite\dwrite_line_metrics1.htm
tech.root: DirectWrite
ms.assetid: 7b5cc425-8a7e-0bff-3fe1-73984872b60b
ms.date: 09/10/2025
ms.keywords: DWRITE_LINE_METRICS1, DWRITE_LINE_METRICS1 structure [Direct Write], directwrite.dwrite_line_metrics1, dwrite_3/DWRITE_LINE_METRICS1
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - DWRITE_LINE_METRICS1
 - dwrite_3/DWRITE_LINE_METRICS1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite_3.h
api_name:
 - DWRITE_LINE_METRICS1
---

## -description

Contains information about a formatted line of text.

## -struct-fields

### -field leadingBefore

Type: <b>FLOAT</b>

White space before the content of the line. This is included in the line height and baseline distances.
If the line is formatted horizontally either with a uniform line spacing or with proportional
line spacing, this value represents the extra space above the content.

### -field leadingAfter

Type: <b>FLOAT</b>

White space after the content of the line. This is included in the height of the line.
If the line is formatted horizontally either with a uniform line spacing or with proportional
line spacing, this value represents the extra space below the content.
