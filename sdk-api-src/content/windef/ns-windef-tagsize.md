---
UID: NS:windef.tagSIZE
title: tagSIZE
author: windows-sdk-content
description: The SIZE structure defines the width and height of a rectangle.
old-location: display\size.htm
tech.root: display
ms.assetid: 08d81096-069f-4554-9bb9-d4a37c0950ac
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: "*LPSIZE, *PSIZE, *PSIZEL, LPSIZE, LPSIZE structure pointer [Display Devices], PSIZE, PSIZE structure pointer [Display Devices], SIZE, SIZE structure [Display Devices], SIZEL, display.size, grstrcts_2697a459-d1f4-4617-8370-d51a3c79f609.xml, tagSIZE, windef/LPSIZE, windef/PSIZE, windef/SIZE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: windef.h
req.include-header: Windows.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - windef.h
api_name:
 - SIZE
product: Windows
targetos: Windows
req.typenames: SIZE, *PSIZE, *LPSIZE
req.redist: 
---

# tagSIZE structure


## -description


The SIZE structure defines the width and height of a rectangle.


## -struct-fields




### -field cx

Specifies the rectangle's width. The units depend on which function uses this structure. 


### -field cy

Specifies the rectangle's height. The units depend on which function uses this structure.


## -remarks



The rectangle dimensions stored in this structure can correspond to viewport extents, window extents, text extents, bitmap dimensions, or the aspect-ratio filter for some extended functions.




## -see-also




<a href="https://msdn.microsoft.com/a44f33f4-49b2-4a36-a7bd-fc4a9d3a3943">RECT</a>



<a href="https://msdn.microsoft.com/709f8262-829e-4cda-bb0b-564307edfd24">RECTL</a>
 

 

