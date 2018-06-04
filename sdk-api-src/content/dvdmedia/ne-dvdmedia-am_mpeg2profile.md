---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# AM_MPEG2Profile enumeration


## -description



Indicates an MPEG-2 video profile as specified in the MPEG-2 video standard (ISO13818-2).




## -enum-fields




### -field AM_MPEG2Profile_Simple


            Simple profile.
          


### -field AM_MPEG2Profile_Main


            Main profile.
          


### -field AM_MPEG2Profile_SNRScalable


            Signal to Noise Ratio (SNR) scalable profile
          


### -field AM_MPEG2Profile_SpatiallyScalable


            Spatially scalable profile.
          


### -field AM_MPEG2Profile_High


            High profile.
          


## -remarks



DVD video decoders should support <b>AM_MPEG2Profile_Simple</b> or <b>AM_MPEG2Profile_Main</b>.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>
 

 

