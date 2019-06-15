---
UID: NE:codecapi.eAVEncVideoColorLighting
title: eAVEncVideoColorLighting (codecapi.h)
author: windows-sdk-content
description: Specifies the intended lighting conditions for viewing a video source. This enumeration is used with the AVEncVideoInputColorLighting and AVEncVideoOutputColorLighting properties.
old-location: dshow\eavencvideocolorlighting.htm
tech.root: DirectShow
ms.assetid: d2e85b3e-b458-4148-b9d7-0ed3d4213838
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncVideoColorLighting, codecapi/eAVEncVideoColorLighting_Bright, codecapi/eAVEncVideoColorLighting_Dark, codecapi/eAVEncVideoColorLighting_Dim, codecapi/eAVEncVideoColorLighting_Office, codecapi/eAVEncVideoColorLighting_SameAsSource, codecapi/eAVEncVideoColorLighting_Unknown, dshow.eavencvideocolorlighting, eAVEncVideoColorLighting, eAVEncVideoColorLighting enumeration [DirectShow], eAVEncVideoColorLightingEnumeration, eAVEncVideoColorLighting_Bright, eAVEncVideoColorLighting_Dark, eAVEncVideoColorLighting_Dim, eAVEncVideoColorLighting_Office, eAVEncVideoColorLighting_SameAsSource, eAVEncVideoColorLighting_Unknown
ms.topic: enum
f1_keywords: ["codecapi/eAVEncVideoColorLighting"]
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - codecapi.h
api_name:
 - eAVEncVideoColorLighting
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# eAVEncVideoColorLighting enumeration


## -description



Specifies the intended lighting conditions for viewing a video source. This enumeration is used with the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/avencvideoinputcolorlighting-property">AVEncVideoInputColorLighting</a> and <a href="https://docs.microsoft.com/windows/desktop/DirectShow/avencvideooutputcolorlighting-property">AVEncVideoOutputColorLighting</a> properties.




## -enum-fields




### -field eAVEncVideoColorLighting_SameAsSource

Use the same lighting as the input video. This flag applies to the <b>AVEncVideoOutputColorLighting</b> property only.


### -field eAVEncVideoColorLighting_Unknown

The optimal lighting is unknown.


### -field eAVEncVideoColorLighting_Bright

Bright lighting; for example, outdoors.


### -field eAVEncVideoColorLighting_Office

Medium brightness; for example, normal office lighting.


### -field eAVEncVideoColorLighting_Dim

Dim; for example, a living room with a television and additional low lighting.


### -field eAVEncVideoColorLighting_Dark

Dark; for example, a movie theater.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
 

 

