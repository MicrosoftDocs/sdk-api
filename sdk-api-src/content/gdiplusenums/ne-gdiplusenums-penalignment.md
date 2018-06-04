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

# PenAlignment enumeration


## -description


The <b>PenAlignment</b> enumeration specifies the alignment of a pen relative to the stroke that is being drawn.


## -enum-fields




### -field PenAlignmentCenter

Specifies that the pen is aligned on the center of the line that is drawn. 


### -field PenAlignmentInset

Specifies, when drawing a polygon, that the pen is aligned on the inside of the edge of the polygon. 


## -remarks



If you set the alignment of a 
				<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object to <b><b>PenAlignmentInset</b></b>, you cannot use that pen to draw compound lines or triangular dash caps.



