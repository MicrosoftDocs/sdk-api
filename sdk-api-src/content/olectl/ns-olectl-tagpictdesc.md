---
UID: NS:olectl.tagPICTDESC
title: tagPICTDESC
author: windows-sdk-content
description: Contains parameters to create a picture object through the OleCreatePictureIndirect function.
old-location: com\pictdesc.htm
tech.root: com
ms.assetid: eb1f1de7-dcfe-4c1c-8737-f5ab4d7977d6
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*LPPICTDESC, LPPICTDESC, LPPICTDESC structure pointer [COM], PICTDESC, PICTDESC structure [COM], _ctrl_PICTDESC, com.pictdesc, olectl/LPPICTDESC, olectl/PICTDESC, tagPICTDESC"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: olectl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Olectl.h
api_name:
 - PICTDESC
product: Windows
targetos: Windows
req.typenames: PICTDESC, *LPPICTDESC
req.redist: 
---

# tagPICTDESC structure


## -description


Contains parameters to create a picture object through the <a href="https://msdn.microsoft.com/fb021348-07d4-4974-a71e-abb1b8d760c4">OleCreatePictureIndirect</a> function.


## -struct-fields




### -field cbSizeofstruct

The size of the structure, in bytes.


### -field picType

Type of picture described by this structure, which can be any value from the <a href="https://msdn.microsoft.com/79f10687-f0eb-4b5e-a1a9-9186dbd0b51f">PICTYPE</a> enumeration. This selects the arm of the union that corresponds to one of the picture type structures below.


### -field bmp

Structure containing bitmap information if <b>picType</b> is <b>PICTYPE_BITMAP</b>.


### -field bmp.hbitmap

The <b>HBITMAP</b> handle identifying the bitmap assigned to the picture object.


### -field bmp.hpal

The <b>HPALETTE</b> handle identifying the color palette for the bitmap.


### -field wmf

Structure containing metafile information if <b>picType</b> is <b>PICTYPE_METAFILE</b>.


### -field wmf.hmeta

The <b>HMETAFILE</b> handle identifying the metafile assigned to the picture object.


### -field wmf.xExt

Horizontal extent of the metafile in TWIPS units.


### -field wmf.yExt

Vertical extent of the metafile in TWIPS units.


### -field icon

Identifies a structure containing icon information if <b>picType</b> is <b>PICTYPE_ICON</b>.


### -field icon.hicon

The <b>HICON</b> handle identifying the icon assigned to the picture object.


### -field emf

Structure containing enhanced metafile information if <b>picType</b> is <b>PICTYPE_ENHMETAFILE</b>.


### -field emf.hemf

The <b>HENHMETAFILE</b> handle identifying the enhanced metafile assigned to the picture object.


## -see-also




<a href="https://msdn.microsoft.com/fb021348-07d4-4974-a71e-abb1b8d760c4">OleCreatePictureIndirect</a>



<a href="https://msdn.microsoft.com/79f10687-f0eb-4b5e-a1a9-9186dbd0b51f">PICTYPE</a>
 

 

