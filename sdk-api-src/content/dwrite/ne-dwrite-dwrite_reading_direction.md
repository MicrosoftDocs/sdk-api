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

# DWRITE_READING_DIRECTION enumeration


## -description



    Specifies the direction in which reading progresses.
  
<div class="alert"><b>Note</b>  <b>DWRITE_READING_DIRECTION_TOP_TO_BOTTOM</b> and <b>DWRITE_READING_DIRECTION_BOTTOM_TO_TOP</b> are available in Windows 8.1 and later, only.</div><div> </div>

## -enum-fields




### -field DWRITE_READING_DIRECTION_LEFT_TO_RIGHT

Indicates that reading progresses from left to right.


### -field DWRITE_READING_DIRECTION_RIGHT_TO_LEFT

Indicates that reading progresses from right to left.


### -field DWRITE_READING_DIRECTION_TOP_TO_BOTTOM

<div class="alert"><b>Note</b>  Windows 8.1 and later only.</div>
<div> </div>
Indicates that reading progresses from top to bottom.


### -field DWRITE_READING_DIRECTION_BOTTOM_TO_TOP

<div class="alert"><b>Note</b>  Windows 8.1 and later only.</div>
<div> </div>
 Indicates that reading progresses from bottom to top.

