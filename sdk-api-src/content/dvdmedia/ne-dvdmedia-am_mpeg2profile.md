---
UID: NE:dvdmedia.AM_MPEG2Profile
title: AM_MPEG2Profile
author: windows-sdk-content
description: Indicates an MPEG-2 video profile as specified in the MPEG-2 video standard (ISO13818-2).
old-location: dshow\am_mpeg2profile.htm
old-project: DirectShow
ms.assetid: 1f03a556-feb7-40c7-a3df-818de6873049
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: AM_MPEG2Profile, AM_MPEG2Profile enumeration [DirectShow], AM_MPEG2Profile_High, AM_MPEG2Profile_Main, AM_MPEG2Profile_SNRScalable, AM_MPEG2Profile_Simple, AM_MPEG2Profile_SpatiallyScalable, MPEG2ProfileEnumeration, dshow.am_mpeg2profile, dvdmedia/AM_MPEG2Profile, dvdmedia/AM_MPEG2Profile_High, dvdmedia/AM_MPEG2Profile_Main, dvdmedia/AM_MPEG2Profile_SNRScalable, dvdmedia/AM_MPEG2Profile_Simple, dvdmedia/AM_MPEG2Profile_SpatiallyScalable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: dvdmedia.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dvdmedia.h
api_name:
 - AM_MPEG2Profile
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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
 

 

