---
UID: NS:mfapi._MT_CUSTOM_VIDEO_PRIMARIES
title: "_MT_CUSTOM_VIDEO_PRIMARIES"
author: windows-driver-content
description: Defines custom color primaries for a video source. The color primaries define how to convert colors from RGB color space to CIE XYZ color space.
old-location: mf\mt_custom_video_primaries.htm
old-project: medfound
ms.assetid: 2c26e906-e428-4a76-b10a-10a18f300ebe
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: 2c26e906-e428-4a76-b10a-10a18f300ebe, MT_CUSTOM_VIDEO_PRIMARIES, MT_CUSTOM_VIDEO_PRIMARIES structure [Media Foundation], _MT_CUSTOM_VIDEO_PRIMARIES, mf.mt_custom_video_primaries, mfapi/MT_CUSTOM_VIDEO_PRIMARIES
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mfapi.h
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
req.typenames: MT_CUSTOM_VIDEO_PRIMARIES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mfapi.h
api_name:
-	MT_CUSTOM_VIDEO_PRIMARIES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MT_CUSTOM_VIDEO_PRIMARIES structure


## -description



Defines custom color primaries for a video source. The color primaries define how to convert colors from RGB color space to CIE XYZ color space.




## -struct-fields




### -field fRx

Red x-coordinate.


### -field fRy

Red y-coordinate.


### -field fGx

Green x-coordinate.


### -field fGy

Green y-coordinate.


### -field fBx

Blue x-coordinate.


### -field fBy

Blue y-coordinate.


### -field fWx

White point x-coordinate.


### -field fWy

White point y-coordinate.


## -remarks



This structure is used with the <a href="https://msdn.microsoft.com/dc5df755-53cf-4910-af42-309f1f46b1ed">MF_MT_CUSTOM_VIDEO_PRIMARIES</a> attribute.




## -see-also




<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

