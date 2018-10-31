---
UID: NE:codecapi.eAVEncVideoColorLighting
title: eAVEncVideoColorLighting
author: windows-sdk-content
description: Specifies the intended lighting conditions for viewing a video source. This enumeration is used with the AVEncVideoInputColorLighting and AVEncVideoOutputColorLighting properties.
old-location: dshow\eavencvideocolorlighting.htm
tech.root: DirectShow
ms.assetid: d2e85b3e-b458-4148-b9d7-0ed3d4213838
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: codecapi/eAVEncVideoColorLighting, codecapi/eAVEncVideoColorLighting_Bright, codecapi/eAVEncVideoColorLighting_Dark, codecapi/eAVEncVideoColorLighting_Dim, codecapi/eAVEncVideoColorLighting_Office, codecapi/eAVEncVideoColorLighting_SameAsSource, codecapi/eAVEncVideoColorLighting_Unknown, dshow.eavencvideocolorlighting, eAVEncVideoColorLighting, eAVEncVideoColorLighting enumeration [DirectShow], eAVEncVideoColorLightingEnumeration, eAVEncVideoColorLighting_Bright, eAVEncVideoColorLighting_Dark, eAVEncVideoColorLighting_Dim, eAVEncVideoColorLighting_Office, eAVEncVideoColorLighting_SameAsSource, eAVEncVideoColorLighting_Unknown
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
---

# eAVEncVideoColorLighting enumeration


## -description



Specifies the intended lighting conditions for viewing a video source. This enumeration is used with the <a href="https://msdn.microsoft.com/718a6d56-c869-4340-bbb8-cac5b231c37e">AVEncVideoInputColorLighting</a> and <a href="https://msdn.microsoft.com/67b69d02-db5d-474c-9df4-146c5283d76e">AVEncVideoOutputColorLighting</a> properties.




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




<a href="https://msdn.microsoft.com/en-us/library/Dd387884(v=VS.85).aspx">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd311953(v=VS.85).aspx">ICodecAPI Interface</a>
 

 

