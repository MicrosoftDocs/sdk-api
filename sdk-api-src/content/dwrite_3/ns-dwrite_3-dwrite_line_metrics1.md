---
UID: NS:dwrite_3.DWRITE_LINE_METRICS1
title: DWRITE_LINE_METRICS1 (dwrite_3.h)
author: windows-sdk-content
description: Contains information about a formatted line of text.
old-location: directwrite\dwrite_line_metrics1.htm
tech.root: DirectWrite
ms.assetid: 7b5cc425-8a7e-0bff-3fe1-73984872b60b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DWRITE_LINE_METRICS1, DWRITE_LINE_METRICS1 structure [Direct Write], directwrite.dwrite_line_metrics1, dwrite_3/DWRITE_LINE_METRICS1
ms.topic: struct
req.header: dwrite_3.h
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
 - dwrite_3.h
api_name:
 - DWRITE_LINE_METRICS1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DWRITE_LINE_METRICS1 structure


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


### -field DWRITE_LINE_METRICS

 




#### - baseline

Type: <b>FLOAT</b>

The distance from the top of the text line to its baseline.


#### - height

Type: <b>FLOAT</b>

The height of the text line.


#### - isTrimmed

Type: <b>BOOL</b>

The line is trimmed.


#### - length

Type: <b>UINT32</b>

The number of text positions in the text line. 
	  This includes any trailing whitespace and newline characters.


#### - newlineLength

Type: <b>UINT32</b>

The number of characters in the newline sequence at the end of the text line. 
	  If the count is zero, then the text line was either wrapped or it is the end of the text.


#### - trailingWhitespaceLength

Type: <b>UINT32</b>

The number of whitespace positions at the end of the text line. 
	  Newline sequences are considered whitespace.

