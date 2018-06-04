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

# DWRITE_FONT_FILE_TYPE enumeration


## -description


The type of a font represented by a single font file. Font formats that consist of multiple files, for example Type 1 .PFM and .PFB, have separate enum values for each of the file types.


## -enum-fields




### -field DWRITE_FONT_FILE_TYPE_UNKNOWN

Font type is not recognized by the DirectWrite font system.


### -field DWRITE_FONT_FILE_TYPE_CFF

OpenType font with CFF outlines.


### -field DWRITE_FONT_FILE_TYPE_TRUETYPE

OpenType font with TrueType outlines.


### -field DWRITE_FONT_FILE_TYPE_OPENTYPE_COLLECTION


### -field DWRITE_FONT_FILE_TYPE_TYPE1_PFM

Type 1 PFM font.


### -field DWRITE_FONT_FILE_TYPE_TYPE1_PFB

Type 1 PFB font.


### -field DWRITE_FONT_FILE_TYPE_VECTOR

Vector .FON font.


### -field DWRITE_FONT_FILE_TYPE_BITMAP

Bitmap .FON font.


### -field DWRITE_FONT_FILE_TYPE_TRUETYPE_COLLECTION

OpenType font that contains a TrueType collection.

