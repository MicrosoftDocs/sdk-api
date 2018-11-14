---
UID: NS:magnification.tagMAGCOLOREFFECT
title: tagMAGCOLOREFFECT
author: windows-sdk-content
description: Describes a color transformation matrix that a magnifier control uses to apply a color effect to magnified screen content.
old-location: magapi\magapi_magcoloreffect.htm
tech.root: magapi
ms.assetid: VS|magapi|~\magapi\reference\structures\magcoloreffectstruct.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PMAGCOLOREFFECT, MAGCOLOREFFECT, MAGCOLOREFFECT structure [Magnification API], PMAGCOLOREFFECT, PMAGCOLOREFFECT structure pointer [Magnification API], magapi.magapi_magcoloreffect, magapi_magcoloreffect, magnification/MAGCOLOREFFECT, magnification/PMAGCOLOREFFECT, tagMAGCOLOREFFECT"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: magnification.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Magnification.h
api_name:
 - MAGCOLOREFFECT
product: Windows
targetos: Windows
req.typenames: MAGCOLOREFFECT, *PMAGCOLOREFFECT
req.redist: 
---

# tagMAGCOLOREFFECT structure


## -description


Describes a color transformation matrix that a magnifier control uses to apply a color effect to magnified screen content.


## -struct-fields




### -field transform

 




#### - transform[5][5]

Type: <b>float</b>

The color transformation matrix.


## -remarks



The values in the matrix are for red, blue, green, alpha, and color translation. For more information, see 
<a href="https://msdn.microsoft.com/fcd7f3d9-8bad-44f8-8c9c-c2f5df4a7241">Using a Color Matrix to Transform a Single Color</a> in the Windows GDI+ documentation.
 





## -see-also




<a href="https://msdn.microsoft.com/d86d3e43-5da0-460c-b243-d0797f5d0911">MagGetColorEffect</a>



<a href="https://msdn.microsoft.com/53749109-5370-45e7-ba90-79ad1504c41e">MagSetColorEffect</a>



<b>Reference</b>
 

 

