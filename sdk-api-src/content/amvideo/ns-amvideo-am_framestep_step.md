---
UID: NS:amvideo._AM_FRAMESTEP_STEP
title: AM_FRAMESTEP_STEP (amvideo.h)
author: windows-sdk-content
description: Specifies the number of frames to step.
old-location: dshow\am_property_framestep.htm
tech.root: DirectShow
ms.assetid: 342029c8-0b2b-45d2-852d-062a8d297d28
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AM_FRAMESTEP_STEP, AM_FRAMESTEP_STEP structure [DirectShow], AM_PROPERTY_FRAMESTEPStructure, _AM_FRAMESTEP_STEP, amvideo/AM_FRAMESTEP_STEP, dshow.am_property_framestep
ms.topic: struct
f1_keywords: 
 - "amvideo/AM_FRAMESTEP_STEP"
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
 - AM_FRAMESTEP_STEP
product: Windows
targetos: Windows
req.typenames: AM_FRAMESTEP_STEP
req.redist: 
ms.custom: 19H1
---

# AM_FRAMESTEP_STEP structure


## -description



Specifies the number of frames to step.




## -struct-fields




### -field dwFramesToStep

<b>DWORD</b> value specifying to the decoder the number of frames to step. Must be at least 1. If greater than 1, this instruction means to skip <i>n</i> - 1 frames and show the <i>n</i>th.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/frame-stepping-property-set">Frame Stepping Property Set</a>
 

 

