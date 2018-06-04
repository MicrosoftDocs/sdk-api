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

# DWRITE_HIT_TEST_METRICS structure


## -description


Describes the region obtained by a hit test.


## -struct-fields




### -field textPosition

Type: <b>UINT32</b>

The first text position within the hit region. 


### -field length

Type: <b>UINT32</b>

The number of text positions within the hit region. 


### -field left

Type: <b>FLOAT</b>

The x-coordinate of the upper-left corner of the hit region.


### -field top

Type: <b>FLOAT</b>

The y-coordinate of the upper-left corner of the hit region.


### -field width

Type: <b>FLOAT</b>

The width of the hit region.


### -field height

Type: <b>FLOAT</b>

The height of the hit region.


### -field bidiLevel

Type: <b>UINT32</b>

The <a href="https://msdn.microsoft.com/413d49d2-bacd-4e98-bfac-c0aea2650a7c">BIDI level</a> of the text positions within the hit region.


### -field isText

Type: <b>BOOL</b>

true if the hit region contains text; otherwise, false.


### -field isTrimmed

Type: <b>BOOL</b>

true if the text range is trimmed; otherwise, false.

