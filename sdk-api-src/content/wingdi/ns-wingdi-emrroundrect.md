---
UID: NS:wingdi.tagEMRROUNDRECT
title: EMRROUNDRECT (wingdi.h)
author: windows-sdk-content
description: The EMRROUNDRECT structure contains members for the RoundRect enhanced metafile record.
old-location: gdi\emrroundrect.htm
tech.root: gdi
ms.assetid: 74caff9e-6882-4585-ad51-e83e4afb8454
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PEMRROUNDRECT, EMRROUNDRECT, EMRROUNDRECT structure [Windows GDI], PEMRROUNDRECT, PEMRROUNDRECT structure pointer [Windows GDI], _win32_EMRROUNDRECT_str, gdi.emrroundrect, wingdi/EMRROUNDRECT, wingdi/PEMRROUNDRECT"
ms.topic: struct
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Wingdi.h
api_name:
 - EMRROUNDRECT
product: Windows
targetos: Windows
req.typenames: EMRROUNDRECT, *PEMRROUNDRECT
req.redist: 
ms.custom: 19H1
---

# EMRROUNDRECT structure


## -description



The <b>EMRROUNDRECT</b> structure contains members for the <b>RoundRect</b> enhanced metafile record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field rclBox

Bounding rectangle, in logical units.


### -field szlCorner

Width and height, in logical units, of the ellipse used to draw rounded corners.


## -see-also




<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/17808a6a-7bd0-4fd6-81ab-00d5db764b93">RoundRect</a>
 

 

