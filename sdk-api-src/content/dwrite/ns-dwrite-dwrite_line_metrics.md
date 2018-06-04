---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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

