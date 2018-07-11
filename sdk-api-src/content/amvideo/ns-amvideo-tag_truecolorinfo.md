---
UID: NS:amvideo.tag_TRUECOLORINFO
title: tag_TRUECOLORINFO
author: windows-sdk-content
description: The TRUECOLORINFO structure contains color palette and bitmask information for a video image.
old-location: dshow\truecolorinfostructure.htm
old-project: DirectShow
ms.assetid: 8269d8c2-ff8e-48e0-b4f6-06900a7ecfdc
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: TRUECOLORINFO, TRUECOLORINFO structure [DirectShow], TRUECOLORINFOStructure, amvideo/TRUECOLORINFO, dshow.truecolorinfostructure, tag_TRUECOLORINFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: amvideo.h
req.include-header: Dshow.h
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
req.typenames: TRUECOLORINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - amvideo.h
api_name:
 - TRUECOLORINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tag_TRUECOLORINFO structure


## -description



          The <b>TRUECOLORINFO</b> structure contains color palette and bitmask information for a video image.
        


## -struct-fields




### -field dwBitMasks


            Array of color masks (one per color element).
          


### -field bmiColors


            Array of palette colors.
          


## -remarks



This structure is not used for some RGB formats. For more information about which fields are valid under different circumstances, see the Platform SDK documentation for <b>BITMAPINFO</b>.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/f08a449c-fed4-400b-a2fc-817bd59ba3fd">VIDEOINFO</a>
 

 

