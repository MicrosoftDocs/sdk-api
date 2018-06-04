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
 

 

