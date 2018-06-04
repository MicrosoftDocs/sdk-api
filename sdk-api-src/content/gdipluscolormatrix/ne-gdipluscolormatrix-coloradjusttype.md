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

# ColorAdjustType enumeration


## -description


The <b>ColorAdjustType</b> enumeration specifies which GDI+ objects use color-adjustment information. You can adjust the colors in a rendered image by passing the address of an 
			<a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a> object to the 
			<a href="https://msdn.microsoft.com/c9577988-e52f-4f71-ab1b-51bb5368812e">Graphics::DrawImage</a> method. An 
			<b>ImageAttributes</b> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. Several of the methods of the 
			<b>ImageAttributes</b> class receive an element of the <b>ColorAdjustType</b> enumeration to specify the adjustment category.


## -enum-fields




### -field ColorAdjustTypeDefault

Specifies that color or grayscale adjustment applies to all categories that do not have adjustment settings of their own. 


### -field ColorAdjustTypeBitmap

Specifies that color or grayscale adjustment applies to bitmapped images. 


### -field ColorAdjustTypeBrush

Specifies that color or grayscale adjustment applies to brush operations in metafiles. 


### -field ColorAdjustTypePen

Specifies that color or grayscale adjustment applies to pen operations in metafiles. 


### -field ColorAdjustTypeText

Specifies that color or grayscale adjustment applies to text drawn in metafiles. 


### -field ColorAdjustTypeCount

Used internally to record the number of color adjustment types.


### -field ColorAdjustTypeAny

Reserved

