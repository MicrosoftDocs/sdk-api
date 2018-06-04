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

# DriverStringOptions enumeration


## -description


The <b>DriverStringOptions</b> enumeration specifies the spacing, orientation, and quality of the rendering for driver strings.


## -enum-fields




### -field DriverStringOptionsCmapLookup

Specifies that the string array contains Unicode character values. 
			If this flag is not set, each value in array is interpreted as an index to a font glyph that defines a character to be displayed.


### -field DriverStringOptionsVertical

Specifies that the string is displayed vertically. 


### -field DriverStringOptionsRealizedAdvance

Specifies that the glyph positions are calculated from the position of the first glyph. If this flag is not set, the glyph positions are obtained from an array of coordinates. 


### -field DriverStringOptionsLimitSubpixel

Specifies that less memory should be used for cache of antialiased glyphs. This also produces lower quality. If this flag isn't set, more memory is used, but the quality is higher. 


## -see-also




<a href="https://msdn.microsoft.com/780d97ec-f446-4d19-837f-517a7d6dd27d">Antialiasing with Text</a>



<a href="https://msdn.microsoft.com/daed7b4e-5284-4a38-bd33-274618f01027">Graphics::DrawDriverString</a>



<a href="https://msdn.microsoft.com/f68ee34e-84e9-4af1-b5f7-018b875d80ad">Graphics::MeasureDriverString</a>
 

 

