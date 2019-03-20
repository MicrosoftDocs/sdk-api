---
UID: NE:gdiplusenums.ObjectType
title: ObjectType (gdiplusenums.h)
author: windows-sdk-content
description: The ObjectType enumeration indicates the object type value of an EMF+ record.
old-location: gdiplus\_gdiplus_ENUM_ObjectType.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\objecttype.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ObjectType, ObjectType enumeration [GDI+], ObjectTypeBrush, ObjectTypeCustomLineCap, ObjectTypeFont, ObjectTypeGraphics, ObjectTypeImageAttributes, ObjectTypeInvalid, ObjectTypeMax, ObjectTypeMin, ObjectTypePath, ObjectTypePen, ObjectTypeRegion, ObjectTypeStringFormat, _gdiplus_ENUM_ObjectType, gdiplus._gdiplus_ENUM_ObjectType, gdiplusenums/ObjectType, gdiplusenums/ObjectTypeBrush, gdiplusenums/ObjectTypeCustomLineCap, gdiplusenums/ObjectTypeFont, gdiplusenums/ObjectTypeGraphics, gdiplusenums/ObjectTypeImageAttributes, gdiplusenums/ObjectTypeInvalid, gdiplusenums/ObjectTypeMax, gdiplusenums/ObjectTypeMin, gdiplusenums/ObjectTypePath, gdiplusenums/ObjectTypePen, gdiplusenums/ObjectTypeRegion, gdiplusenums/ObjectTypeStringFormat
ms.topic: enum
req.header: gdiplusenums.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusenums.h
api_name:
 - ObjectType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# ObjectType enumeration


## -description


The <b>ObjectType</b> enumeration indicates the object type value of an EMF+ record.


## -enum-fields




### -field ObjectTypeInvalid

Object type is invalid.


### -field ObjectTypeBrush

Object type is a brush.


### -field ObjectTypePen

Object type is a pen.


### -field ObjectTypePath

Object type is a path.


### -field ObjectTypeRegion

Object type is a region.


### -field ObjectTypeImage


### -field ObjectTypeFont

Object type is a font.


### -field ObjectTypeStringFormat

Object type is a string format.


### -field ObjectTypeImageAttributes

Object type is an image attribute.


### -field ObjectTypeCustomLineCap

Object type is a custom line cap.


### -field ObjectTypeGraphics

Object type is graphics.


### -field ObjectTypeMax

Maximum enumeration value. Currently, it is ObjectTypeGraphics.


### -field ObjectTypeMin

Minimum enumeration value. Currently, it is ObjectTypeBrush.


## -remarks



To determine whether the object type value of an EMF+ record is valid, call <a href="https://msdn.microsoft.com/en-us/library/ms534087(v=VS.85).aspx">ObjectTypeIsValid</a>.



