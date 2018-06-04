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



To determine whether the object type value of an EMF+ record is valid, call <a href="https://msdn.microsoft.com/7cfdbad5-3d32-4383-85da-cfe338f1664e">ObjectTypeIsValid</a>.



