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

# DWRITE_FONT_FACE_TYPE enumeration


## -description


Indicates the file format of a complete font face.


## -enum-fields




### -field DWRITE_FONT_FACE_TYPE_CFF

OpenType font face with CFF outlines.


### -field DWRITE_FONT_FACE_TYPE_TRUETYPE

OpenType font face with TrueType outlines.


### -field DWRITE_FONT_FACE_TYPE_OPENTYPE_COLLECTION


### -field DWRITE_FONT_FACE_TYPE_TYPE1

A Type 1 font face.


### -field DWRITE_FONT_FACE_TYPE_VECTOR

A vector .FON format font face.


### -field DWRITE_FONT_FACE_TYPE_BITMAP

A bitmap .FON format font face.


### -field DWRITE_FONT_FACE_TYPE_UNKNOWN

Font face type is not recognized by the DirectWrite font system.


### -field DWRITE_FONT_FACE_TYPE_RAW_CFF

The font data includes only the CFF table from an OpenType CFF font. This font face type can be used only for embedded fonts (i.e., custom font file loaders) and the resulting font face object supports only the minimum functionality necessary to render glyphs.


### -field DWRITE_FONT_FACE_TYPE_TRUETYPE_COLLECTION

OpenType font face that is a part of a TrueType collection.


## -remarks



Font formats that consist of multiple files, such as Type 1 .PFM and .PFB, have a single enum entry.



