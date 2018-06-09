---
UID: NE:dvdevcod._tagDVD_WARNING
title: "_tagDVD_WARNING"
author: windows-sdk-content
description: Specifies DVD warning conditions.
old-location: dshow\dvd_warning.htm
old-project: DirectShow
ms.assetid: e36904de-a28f-4372-8ed1-6b7f38e7dd5e
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: DVD_WARNING, DVD_WARNING , DVD_WARNING enumeration [DirectShow], DVD_WARNINGEnumeration, DVD_WARNING_FormatNotSupported, DVD_WARNING_IllegalNavCommand, DVD_WARNING_InvalidDVD1_0Disc, DVD_WARNING_Open, DVD_WARNING_Read, DVD_WARNING_Seek, _tagDVD_WARNING, dshow.dvd_warning, dvdevcod/DVD_WARNING, dvdevcod/DVD_WARNING_FormatNotSupported, dvdevcod/DVD_WARNING_IllegalNavCommand, dvdevcod/DVD_WARNING_InvalidDVD1_0Disc, dvdevcod/DVD_WARNING_Open, dvdevcod/DVD_WARNING_Read, dvdevcod/DVD_WARNING_Seek
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: dvdevcod.h
req.include-header: Dshow.h
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
req.typenames: DVD_WARNING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dvdevcod.h
api_name:
 - DVD_WARNING
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _tagDVD_WARNING enumeration


## -description



Specifies DVD warning conditions.




## -enum-fields




### -field DVD_WARNING_InvalidDVD1_0Disc


            DVD-Video disc is authored incorrectly. Playback can continue, but unexpected behavior might occur.
          


### -field DVD_WARNING_FormatNotSupported


            A decoder would not support the current format. Playback of a stream (audio, video or subpicture) might not function. <i>lParam2</i> of the <a href="https://msdn.microsoft.com/d7221e8a-089f-4eaf-a193-548709c14336">EC_DVD_WARNING</a> event notification code contains the stream type (see <a href="https://msdn.microsoft.com/3fb3e57f-7c0b-4a49-b83d-798c84b2d5d1">AM_DVD_STREAM_FLAGS</a>).
          


### -field DVD_WARNING_IllegalNavCommand


            The internal DVD navigation command processor attempted to process an illegal command.
          


### -field DVD_WARNING_Open


            File Open failed.
          


### -field DVD_WARNING_Seek


            File Seek failed.
          


### -field DVD_WARNING_Read


            File Read failed.
          


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/d7221e8a-089f-4eaf-a193-548709c14336">EC_DVD_WARNING</a>
 

 

