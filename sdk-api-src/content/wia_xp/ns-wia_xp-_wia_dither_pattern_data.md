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

# _WIA_DITHER_PATTERN_DATA structure


## -description


The <b>WIA_DITHER_PATTERN_DATA</b> structure specifies a dither pattern for scanners. It is used in conjunction with the <a href="https://msdn.microsoft.com/78caa3af-927b-4143-9e88-4b5c918d00a4">scanner device property constant</a> WIA_DPS_DITHER_PATTERN_DATA.


## -struct-fields




### -field lSize

Type: <b>LONG</b>

Specifies the size of this structure in bytes. Should be set to <b>sizeof(WIA_DITHER_PATTERN_DATA)</b>.


### -field bstrPatternName

Type: <b>BSTR</b>

Specifies a string that contains the name of this dither pattern.


### -field lPatternWidth

Type: <b>LONG</b>

Indicates the width of the dither pattern in bytes.


### -field lPatternLength

Type: <b>LONG</b>

Indicates the length of the dither pattern in bytes.


### -field cbPattern

Type: <b>LONG</b>

Specifies the total number of bytes in the array pointed to by the <b>pbPattern</b> member.


### -field pbPattern

Type: <b>BYTE*</b>

Specifies a pointer to a buffer that contains the dither pattern.

