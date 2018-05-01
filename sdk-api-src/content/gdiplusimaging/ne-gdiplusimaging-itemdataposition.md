---
UID: NE:gdiplusimaging.ItemDataPosition
title: ItemDataPosition
author: windows-driver-content
description: The ItemDataPosition enumeration is used to specify the location of custom metadata in an image file.
old-location: gdiplus\_gdiplus_ENUM_ItemDataPosition.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\itemdataposition.htm
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: ItemDataPosition, ItemDataPosition enumeration [GDI+], ItemDataPositionAfterBits, ItemDataPositionAfterHeader, ItemDataPositionAfterPalette, _gdiplus_ENUM_ItemDataPosition, gdiplus._gdiplus_ENUM_ItemDataPosition, gdiplusimaging/ItemDataPosition, gdiplusimaging/ItemDataPositionAfterBits, gdiplusimaging/ItemDataPositionAfterHeader, gdiplusimaging/ItemDataPositionAfterPalette
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: gdiplusimaging.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	GdiplusImaging.h
api_name:
-	ItemDataPosition
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ItemDataPosition enumeration


## -description


The <b>ItemDataPosition</b> enumeration is used to specify the location of custom metadata in an image file. 


## -enum-fields




### -field ItemDataPositionAfterHeader

Specifies that custom metadata is stored after the file header. Valid for JPEG, PNG, and GIF.


### -field ItemDataPositionAfterPalette

Specifies that custom metadata is stored after the palette. Valid for PNG.


### -field ItemDataPositionAfterBits

Specifies that custom metadata is stored after the pixel data. Valid for GIF and PNG.


## -remarks



GDI+ supports custom metadata for JPEG, PNG, and GIF image files.




## -see-also




<a href="https://msdn.microsoft.com/56316228-9cae-46d5-bfef-bbd523aabd2b">ImageItemData</a>
 

 

