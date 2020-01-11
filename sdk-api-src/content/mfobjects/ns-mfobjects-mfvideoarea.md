---
UID: NS:mfobjects._MFVideoArea
title: MFVideoArea (mfobjects.h)
description: Specifies a rectangular area within a video frame.
old-location: mf\mfvideoarea.htm
tech.root: medfound
ms.assetid: d22b8b9c-399b-4fce-a173-833005b5bf03
ms.date: 12/05/2018
ms.keywords: MFVideoArea, MFVideoArea structure [Media Foundation], d22b8b9c-399b-4fce-a173-833005b5bf03, mf.mfvideoarea, mfobjects/MFVideoArea
f1_keywords:
- mfobjects/MFVideoArea
dev_langs:
- c++
req.header: mfobjects.h
req.include-header: Mfidl.h
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
- mfobjects.h
api_name:
- MFVideoArea
targetos: Windows
req.typenames: MFVideoArea
req.redist: 
ms.custom: 19H1
---

# MFVideoArea structure


## -description


Specifies a rectangular area within a video frame.
        


## -struct-fields




### -field OffsetX

An <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/ns-mfobjects-mfoffset">MFOffset</a> structure that contains the x-coordinate of the upper-left corner of the rectangle. This coordinate might have a fractional value.
          


### -field OffsetY

An <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/ns-mfobjects-mfoffset">MFOffset</a> structure that contains the y-coordinate of the upper-left corner of the rectangle. This coordinate might have a fractional value.
          


### -field Area

A <a href="https://docs.microsoft.com/previous-versions/dd145106(v=vs.85)">SIZE</a> structure that contains the width and height of the rectangle.
          


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/ns-mfobjects-mfoffset">MFOffset</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>
 

 

