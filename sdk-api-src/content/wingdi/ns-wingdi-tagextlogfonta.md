---
UID: NS:wingdi.tagEXTLOGFONTA
title: tagEXTLOGFONTA
author: windows-sdk-content
description: The EXTLOGFONT structure defines the attributes of a font.
old-location: gdi\extlogfont.htm
old-project: gdi
ms.assetid: 19f6364e-3347-45b6-be02-e2cc69a7145a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPEXTLOGFONTA, *NPEXTLOGFONTA, *PEXTLOGFONTA, EXTLOGFONT, EXTLOGFONT structure [Windows GDI], EXTLOGFONTA, EXTLOGFONTW, PEXTLOGFONT, PEXTLOGFONT structure pointer [Windows GDI], _win32_EXTLOGFONT_str, gdi.extlogfont, tagEXTLOGFONTA, wingdi/EXTLOGFONT, wingdi/EXTLOGFONTA, wingdi/EXTLOGFONTW, wingdi/PEXTLOGFONT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EXTLOGFONTW (Unicode) and EXTLOGFONTA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: EXTLOGFONTA, *PEXTLOGFONTA, *NPEXTLOGFONTA, *LPEXTLOGFONTA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - EXTLOGFONT
 - EXTLOGFONTA
 - EXTLOGFONTW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

