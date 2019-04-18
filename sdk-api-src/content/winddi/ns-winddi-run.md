---
UID: NS:winddi._RUN
title: RUN (winddi.h)
author: windows-sdk-content
description: The RUN structure is used to describe a linear set of pixels that is not clipped by the CLIPLINE structure.
old-location: display\run.htm
tech.root: display
ms.assetid: 7c53ec29-2541-40d3-95df-bf73d900a6d6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PRUN, PRUN, PRUN structure pointer [Display Devices], RUN, RUN structure [Display Devices], display.run, grstrcts_ccdf6b98-1c92-4d72-b777-e4c075e53064.xml, winddi/PRUN, winddi/RUN"
ms.topic: struct
req.header: winddi.h
req.include-header: Winddi.h
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
 - winddi.h
api_name:
 - RUN
product: Windows
targetos: Windows
req.typenames: RUN, *PRUN
req.redist: 
ms.custom: 19H1
---

# RUN structure


## -description


The RUN structure is used to describe a linear set of pixels that is not clipped by the <a href="https://msdn.microsoft.com/ec938519-3c0c-4664-9e9a-b7fb338920f5">CLIPLINE</a> structure.


## -struct-fields




### -field iStart

Specifies the starting point for a field of pixels to be drawn. The first pixel of the unclipped line is pixel 0.


### -field iStop

Specifies the stopping point for a field of pixels to be drawn.


## -remarks



If the <a href="https://msdn.microsoft.com/ac439eb8-b491-4215-877d-5ee177fbdb39">clip region</a> is complex, a single line segment can be broken into many RUNs. The same segment is returned as many times as necessary to list all of its RUNs.




## -see-also




<a href="https://msdn.microsoft.com/edc64b1e-dd3f-4b6a-858c-91c49a819b0a">PATHOBJ_bEnumClipLines</a>
 

 

