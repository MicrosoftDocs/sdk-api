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

# DWRITE_INLINE_OBJECT_METRICS structure


## -description


Contains properties describing the geometric measurement of an
application-defined inline object.


## -struct-fields




### -field width

Type: <b>FLOAT</b>

The width of the inline object.


### -field height

Type: <b>FLOAT</b>

The height of the inline object.


### -field baseline

Type: <b>FLOAT</b>

The distance from the top of the object to the point where it is lined up with the adjacent text. 
     If the baseline is at the bottom, then <b>baseline</b> simply equals <b>height</b>.


### -field supportsSideways

Type: <b>BOOL</b>

A Boolean flag that indicates whether the object is to be placed upright or alongside the text baseline for vertical text.

