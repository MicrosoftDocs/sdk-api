---
UID: NS:icm.tagCOLOR
title: tagCOLOR
author: windows-driver-content
description: TBD.
old-location: wcs\color.htm
old-project: WCS
ms.assetid: a47ec71f-3605-43d4-a12e-db07aecc0fd0
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: "*PCOLOR, COLOR, COLOR union [Windows Color System], icm/COLOR, tagCOLOR, wcs.color"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: icm.h
req.include-header: 
req.target-type: Windows
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
req.typenames: COLOR
topic_type:
-	kbSyntax
api_type:
-	<TBD>
api_location:
-
api_name:
-	COLOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# tagCOLOR structure


## -description


TBD


## -struct-fields




### -field gray

TBD


### -field rgb

 


### -field cmyk

TBD


### -field XYZ

TBD


### -field Yxy

TBD


### -field Lab

TBD


### -field gen3ch

TBD


### -field named

TBD


### -field hifi

TBD


#### - rbg

TBD


#### - reserved1

TBD


#### - reserved2

TBD


## -remarks



A variable of type COLOR may be accessed as any of the supported color space colors by accessing the appropriate member of the union. For instance, given the following variable declaration:



<code>COLOR aColor;</code>

the red, green and blue values could be set in the following manner:

<code>aColor.rgb.red=100;</code>

<code>aColor.rgb.green=50;</code>

<code>aColor.rgb.blue=2;</code>



