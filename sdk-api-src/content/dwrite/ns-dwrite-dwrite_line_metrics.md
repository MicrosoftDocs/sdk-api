---
UID: NS:dwrite.DWRITE_LINE_METRICS
title: DWRITE_LINE_METRICS (dwrite.h)
description: Contains information about a formatted line of text. (DWRITE_LINE_METRICS)
helpviewer_keywords: ["DWRITE_LINE_METRICS","DWRITE_LINE_METRICS structure [Direct Write]","directwrite.dwrite_line_metrics","dwrite/DWRITE_LINE_METRICS"]
old-location: directwrite\dwrite_line_metrics.htm
tech.root: DirectWrite
ms.assetid: cb589949-2eba-4ebb-ada4-546802fb3d01
ms.date: 12/05/2018
ms.keywords: DWRITE_LINE_METRICS, DWRITE_LINE_METRICS structure [Direct Write], directwrite.dwrite_line_metrics, dwrite/DWRITE_LINE_METRICS
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
 - DWRITE_LINE_METRICS
 - dwrite/DWRITE_LINE_METRICS
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
 - DWRITE_LINE_METRICS
---

# DWRITE_LINE_METRICS structure


## -description

Contains information about a formatted line of text.

## -struct-fields

### -field length

Type: <b>UINT32</b>

The number of text positions in the text line. 
	  This includes any trailing whitespace and newline characters.

### -field trailingWhitespaceLength

Type: <b>UINT32</b>

The number of whitespace positions at the end of the text line. 
	  Newline sequences are considered whitespace.

### -field newlineLength

Type: <b>UINT32</b>

The number of characters in the newline sequence at the end of the text line. 
	  If the count is zero, then the text line was either wrapped or it is the end of the text.

### -field height

Type: <b>FLOAT</b>

The height of the text line.

### -field baseline

Type: <b>FLOAT</b>

The distance from the top of the text line to its baseline.

### -field isTrimmed

Type: <b>BOOL</b>

The line is trimmed.

