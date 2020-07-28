---
UID: NS:amvideo.tag_TRUECOLORINFO
title: TRUECOLORINFO (amvideo.h)
description: The TRUECOLORINFO structure contains color palette and bitmask information for a video image.
helpviewer_keywords: ["TRUECOLORINFO","TRUECOLORINFO structure [DirectShow]","TRUECOLORINFOStructure","amvideo/TRUECOLORINFO","dshow.truecolorinfostructure"]
old-location: dshow\truecolorinfostructure.htm
tech.root: dshow
ms.assetid: 8269d8c2-ff8e-48e0-b4f6-06900a7ecfdc
ms.date: 12/05/2018
ms.keywords: TRUECOLORINFO, TRUECOLORINFO structure [DirectShow], TRUECOLORINFOStructure, amvideo/TRUECOLORINFO, dshow.truecolorinfostructure
f1_keywords:
- amvideo/TRUECOLORINFO
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- amvideo.h
api_name:
- TRUECOLORINFO
targetos: Windows
req.typenames: TRUECOLORINFO
req.redist: 
ms.custom: 19H1
---

# TRUECOLORINFO structure


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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo">VIDEOINFO</a>
 

 

