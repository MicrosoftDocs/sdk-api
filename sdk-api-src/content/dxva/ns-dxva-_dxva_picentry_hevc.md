---
UID: NS:dxva._DXVA_PicEntry_HEVC
title: "_DXVA_PicEntry_HEVC"
author: windows-driver-content
description: Specifies a reference to an uncompressed surface.
old-location: mf\dxva_picentry_hevc.htm
old-project: medfound
ms.assetid: 01F9C9F9-8EB4-49D5-91F0-89B4C40DDDC8
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: "*LPDXVA_PicEntry_HEVC, DXVA_PicEntry_HEVC, DXVA_PicEntry_HEVC structure [Media Foundation], PDXVA_PicEntry_HEVC, PDXVA_PicEntry_HEVC structure pointer [Media Foundation], _DXVA_PicEntry_HEVC, dxva/DXVA_PicEntry_HEVC, dxva/PDXVA_PicEntry_HEVC, mf.dxva_picentry_hevc"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dxva.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DXVA_PicEntry_HEVC, *LPDXVA_PicEntry_HEVC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dxva.h
api_name:
-	DXVA_PicEntry_HEVC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DXVA_PicEntry_HEVC structure


## -description


Specifies a reference to an uncompressed surface.


## -struct-fields




### -field Index7Bits

An index that identifies an uncompressed surface .


### -field AssociatedFlag

Optional 1-bit flag associated with the surface. The meaning of the flag depends on the context. For example, it can specify whether the reference frame is a long-term reference or a short-term reference.


#### - bPicEntry

Accesses the entire 8 bits of the union.


## -see-also




<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

