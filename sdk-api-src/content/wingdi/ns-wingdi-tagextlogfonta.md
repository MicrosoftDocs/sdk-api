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

# tagEXTLOGFONTA structure


## -description



The <b>EXTLOGFONT</b> structure defines the attributes of a font.




## -struct-fields




### -field elfLogFont

Specifies some of the attributes of the specified font. This member is a <a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a> structure.


### -field elfFullName

A unique name for the font (for example, ABCD Font Company TrueType Bold Italic Sans Serif).


### -field elfStyle

The style of the font (for example, Bold Italic).


### -field elfVersion

Reserved. Must be zero.


### -field elfStyleSize

This member only has meaning for hinted fonts. It specifies the point size at which the font is hinted. If set to zero, which is its default value, the font is hinted at the point size corresponding to the <b>lfHeight</b> member of the <a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a> structure specified by <b>elfLogFont</b>.


### -field elfMatch

A unique identifier for an enumerated font. This will be filled in by the graphics device interface (GDI) upon font enumeration.


### -field elfReserved

Reserved; must be zero.


### -field elfVendorId

A 4-byte identifier of the font vendor.


### -field elfCulture

Reserved; must be zero.


### -field elfPanose

A <a href="https://msdn.microsoft.com/18aa4a36-8e47-4e35-973f-376d412ed923">PANOSE</a> structure that specifies the shape of the font. If all members of this structure are set to zero, the <b>elfPanose</b> member is ignored by the font mapper.


## -see-also




<a href="https://msdn.microsoft.com/93726d5c-d4ed-4681-bf45-cb899f195b5d">Font and Text Structures</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a>



<a href="https://msdn.microsoft.com/18aa4a36-8e47-4e35-973f-376d412ed923">PANOSE</a>
 

 

