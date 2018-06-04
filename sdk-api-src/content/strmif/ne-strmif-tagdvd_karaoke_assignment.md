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

# tagDVD_KARAOKE_ASSIGNMENT enumeration


## -description



Defines the speaker configuration for an audio stream.




## -enum-fields




### -field DVD_Assignment_reserved0


            Reserved.
          


### -field DVD_Assignment_reserved1


            Reserved.
          


### -field DVD_Assignment_LR


            The stream is assigned to the left and right speakers.
          


### -field DVD_Assignment_LRM


            The stream is assigned to the left, right, and middle speakers.
          


### -field DVD_Assignment_LR1


            The stream is assigned to the left, right, and audio1 speakers.
          


### -field DVD_Assignment_LRM1


            The stream is assigned to the left, right, middle, and audio1 speakers.
          


### -field DVD_Assignment_LR12


            The stream is assigned to the left, right, and audio2 speakers.
          


### -field DVD_Assignment_LRM12


            The stream is assigned to the left, right, middle, and audio2 speakers.
          


## -remarks



All channels within a stream will use the same speaker configuration, although the channels can be sent to different speakers within this configuration.




## -see-also




<a href="https://msdn.microsoft.com/dffb0b0e-edce-47e7-b9c0-983fdd2c4746">DVD_KaraokeAttributes Structure</a>



<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>
 

 

