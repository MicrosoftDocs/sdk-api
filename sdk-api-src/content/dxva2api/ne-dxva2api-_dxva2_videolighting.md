---
UID: NE:dxva2api._DXVA2_VideoLighting
title: "_DXVA2_VideoLighting"
author: windows-sdk-content
description: Describes the intended lighting conditions for viewing video content.
old-location: mf\dxva2_videolighting.htm
old-project: medfound
ms.assetid: d70e7aa7-f68f-4ee3-bb75-dbe369e68f0e
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: DXVA2_VideoLighting, DXVA2_VideoLighting enumeration [Media Foundation], DXVA2_VideoLightingMask, DXVA2_VideoLighting_Unknown, DXVA2_VideoLighting_bright, DXVA2_VideoLighting_dark, DXVA2_VideoLighting_dim, DXVA2_VideoLighting_office, _DXVA2_VideoLighting, d70e7aa7-f68f-4ee3-bb75-dbe369e68f0e, dxva2api/DXVA2_VideoLighting, dxva2api/DXVA2_VideoLightingMask, dxva2api/DXVA2_VideoLighting_Unknown, dxva2api/DXVA2_VideoLighting_bright, dxva2api/DXVA2_VideoLighting_dark, dxva2api/DXVA2_VideoLighting_dim, dxva2api/DXVA2_VideoLighting_office, mf.dxva2_videolighting
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: dxva2api.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DXVA2_VideoLighting
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxva2api.h
api_name:
 - DXVA2_VideoLighting
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DXVA2_VideoLighting enumeration


## -description


Describes the intended lighting conditions for viewing video content. These flags are used in the <a href="https://msdn.microsoft.com/eba2c56b-8951-4dc5-91ae-1371793ce787">DXVA2_ExtendedFormat</a> structure.


## -enum-fields




### -field DXVA2_VideoLightingMask

Bitmask to validate flag values. This value is not a valid flag.


### -field DXVA2_VideoLighting_Unknown

Unknown. Treat as DXVA2_VideoLighting_dim.


### -field DXVA2_VideoLighting_bright

Outdoor lighting.


### -field DXVA2_VideoLighting_office

Medium brightness; for example, an office.


### -field DXVA2_VideoLighting_dim

Dim; for example, a living room with a television and some additional low lighting.


### -field DXVA2_VideoLighting_dark

Dark; for example, a movie theater.


## -remarks



This enumeration is equivalent to the <b>DXVA_VideoLighting</b> enumeration used in DXVA 1.0.

If you are using the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface to describe the video format, the video lighting is specified in the <a href="https://msdn.microsoft.com/697590e3-898e-4ac9-8390-7b0994b6e571">MF_MT_VIDEO_LIGHTING</a> attribute.




## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

