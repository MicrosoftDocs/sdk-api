---
UID: NE:directmanipulation.DIRECTMANIPULATION_SNAPPOINT_COORDINATE
title: DIRECTMANIPULATION_SNAPPOINT_COORDINATE (directmanipulation.h)
author: windows-sdk-content
description: Defines the coordinate system for a collection of snap points.
old-location: directmanipulation\directmanipulation_snappoint_coordinate.htm
tech.root: directmanipulation
ms.assetid: 954ab792-e2b9-4cc0-a0dc-fcb6c6cdf156
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DIRECTMANIPULATION_COORDINATE_BOUNDARY, DIRECTMANIPULATION_COORDINATE_MIRRORED, DIRECTMANIPULATION_COORDINATE_ORIGIN, DIRECTMANIPULATION_SNAPPOINT_COORDINATE, DIRECTMANIPULATION_SNAPPOINT_COORDINATE enumeration [Direct Manipulation], directmanipulation.directmanipulation_snappoint_coordinate, directmanipulation/DIRECTMANIPULATION_COORDINATE_BOUNDARY, directmanipulation/DIRECTMANIPULATION_COORDINATE_MIRRORED, directmanipulation/DIRECTMANIPULATION_COORDINATE_ORIGIN, directmanipulation/DIRECTMANIPULATION_SNAPPOINT_COORDINATE
ms.topic: enum
f1_keywords: 
 - "directmanipulation/DIRECTMANIPULATION_SNAPPOINT_COORDINATE"
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
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
 - directmanipulation.h
api_name:
 - DIRECTMANIPULATION_SNAPPOINT_COORDINATE
product: Windows
targetos: Windows
req.typenames: DIRECTMANIPULATION_SNAPPOINT_COORDINATE
req.redist: 
ms.custom: 19H1
---

# DIRECTMANIPULATION_SNAPPOINT_COORDINATE enumeration


## -description


Defines the coordinate system for a collection of snap points.


## -enum-fields




### -field DIRECTMANIPULATION_COORDINATE_BOUNDARY

Default. 

Snap points are specified relative to the top and left boundaries of the content unless <b>DIRECTMANIPULATION_COORDINATE_MIRRORED</b> is also specified, in which case they are relative to the bottom and right boundaries of the content. For zoom, the boundary is 1.0f.


### -field DIRECTMANIPULATION_COORDINATE_ORIGIN

Snap points are specified relative to the origin of the viewport.


### -field DIRECTMANIPULATION_COORDINATE_MIRRORED

Snap points are interpreted as specified in the negative direction of the origin. The origin is shifted to the bottom and right of the viewport or content. Cannot be set for zoom.


## -remarks



If <b>DIRECTMANIPULATION_COORDINATE_ORIGIN</b> and <b>DIRECTMANIPULATION_COORDINATE_MIRRORED</b> are both specified, the snap points are interpreted as specified from the bottom and right boundaries of the content (the size of the content - the size of the viewport). This is intended for RTL reading scenarios where content is normally specified and rendered from right-to-left or bottom-to-top.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/directmanipulation/direct-manipulation-enumerations">Direct Manipulation Enumerations</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate">SetSnapCoordinate</a>
 

 

