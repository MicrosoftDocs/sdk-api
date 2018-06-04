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

# DWRITE_GRID_FIT_MODE enumeration


## -description


Specifies whether to enable grid-fitting of glyph outlines (also known as hinting).


## -enum-fields




### -field DWRITE_GRID_FIT_MODE_DEFAULT

Choose grid fitting based on the font's table information.


### -field DWRITE_GRID_FIT_MODE_DISABLED

Always disable grid fitting, using the ideal glyph outlines.


### -field DWRITE_GRID_FIT_MODE_ENABLED

Enable grid fitting, adjusting glyph outlines for device pixel display.

