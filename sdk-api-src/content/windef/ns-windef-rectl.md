---
UID: NS:windef._RECTL
title: RECTL (windef.h)
author: windows-sdk-content
description: The RECTL structure defines a rectangle by the coordinates of its upper-left and lower-right corners.
old-location: display\rectl.htm
tech.root: display
ms.assetid: 709f8262-829e-4cda-bb0b-564307edfd24
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPRECTL, *PRECTL, LPRECTL, LPRECTL structure pointer [Display Devices], PRECTL, PRECTL structure pointer [Display Devices], RECTL, RECTL structure [Display Devices], display.rectl, grstrcts_9ae84b3b-7f9e-4296-a6da-4565cd170470.xml, windef/LPRECTL, windef/PRECTL, windef/RECTL"
ms.topic: struct
f1_keywords: 
 - "windef/RECTL"
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
 - RECTL
product: Windows
targetos: Windows
req.typenames: RECTL, *PRECTL, *LPRECTL
req.redist: 
ms.custom: 19H1
---

# RECTL structure


## -description


The RECTL structure defines a rectangle by the coordinates of its upper-left and lower-right corners.


## -struct-fields




### -field left

Specifies the <i>x</i>-coordinate of the upper-left corner of the rectangle. 


### -field top

Specifies the <i>y</i>-coordinate of the upper-left corner of the rectangle. 


### -field right

Specifies the <i>x</i>-coordinate of the lower-right corner of the rectangle. 


### -field bottom

Specifies the <i>y</i>-coordinate of the lower-right corner of the rectangle. 


## -remarks



The RECTL structure is identical to the <a href="https://docs.microsoft.com/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/windef/ns-windef-rect">RECT</a>
 

 

