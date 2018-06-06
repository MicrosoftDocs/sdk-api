---
UID: NS:windef.tagPOINTS
title: tagPOINTS
author: windows-sdk-content
description: The POINTS structure defines the x- and y-coordinates of a point.
old-location: display\points.htm
old-project: display
ms.assetid: 56d642a0-5281-44aa-af1e-61e1e83186af
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*LPPOINTS, *PPOINTS, LPPOINTS, LPPOINTS structure pointer [Display Devices], POINTS, POINTS structure [Display Devices], PPOINTS, PPOINTS structure pointer [Display Devices], display.points, grstrcts_ae45abcf-f0a0-4fbc-b9b8-f021d8f4f182.xml, tagPOINTS, windef/LPPOINTS, windef/POINTS, windef/PPOINTS"
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
tech.root: 
req.typenames: POINTS, *PPOINTS, *LPPOINTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - windef.h
api_name:
 - POINTS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagPOINTS structure


## -description


The POINTS structure defines the x- and y-coordinates of a point.


## -struct-fields




### -field y

Specifies the <i>y</i>-coordinate of the point. 


### -field x

Specifies the <i>x</i>-coordinate of the point. 


## -remarks



The POINTS structure is similar to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a> structures. The difference is that the members of the POINTS structure are of type SHORT, while those of the other two structures are of type LONG.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a>
 

 

