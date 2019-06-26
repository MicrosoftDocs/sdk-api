---
UID: NS:strmif._VMRVIDEOSTREAMINFO
title: VMRVIDEOSTREAMINFO (strmif.h)
author: windows-sdk-content
description: This topic applies to Windows XP or later. The VMRVIDEOSTREAMINFO structure is used in the VMR-7 filter's call to IVMRImageCompositor::CompositeImage on the image compositor.
old-location: dshow\vmrvideostreaminfo.htm
tech.root: DirectShow
ms.assetid: 1425b3aa-f419-49ee-b262-d8d215466a2c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VMRVIDEOSTREAMINFO, VMRVIDEOSTREAMINFO structure [DirectShow], VMRVIDEOSTREAMINFOStructure, dshow.vmrvideostreaminfo, strmif/VMRVIDEOSTREAMINFO
ms.topic: struct
f1_keywords: 
 - "strmif/VMRVIDEOSTREAMINFO"
req.header: strmif.h
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
 - strmif.h
api_name:
 - VMRVIDEOSTREAMINFO
product: Windows
targetos: Windows
req.typenames: VMRVIDEOSTREAMINFO
req.redist: 
ms.custom: 19H1
---

# VMRVIDEOSTREAMINFO structure


## -description



This topic applies to Windows XP or later.
          

The <code>VMRVIDEOSTREAMINFO</code> structure is used in the VMR-7 filter's call to <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrimagecompositor-compositeimage">IVMRImageCompositor::CompositeImage</a> on the image compositor.




## -struct-fields




### -field pddsVideoSurface

Specifies the DirectDraw surface that contains the video to be composited.


### -field dwWidth

Specifies the width of the video rectangle.


### -field dwHeight

Specifies the height of the video rectangle.


### -field dwStrmID

Specifies the input stream. This value corresponds to the input pin.


### -field fAlpha

Specifies the alpha value for this stream. (Not per-pixel alpha.)


### -field ddClrKey

Specifies the source color key value or -1 if color keying is not to be used for this stream.


### -field rNormal

Specifies the position of the image in composition space.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>
 

 

