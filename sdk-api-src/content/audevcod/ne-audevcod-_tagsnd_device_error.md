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

# _tagSND_DEVICE_ERROR enumeration


## -description



Specifies how the audio device was being accessed when the failure occurred.




## -enum-fields




### -field SNDDEV_ERROR_Open


            The audio device attempted to open.
          


### -field SNDDEV_ERROR_Close


            The audio device attempted to close.
          


### -field SNDDEV_ERROR_GetCaps


            The capabilities of the underlying hardware were being retrieved.
          


### -field SNDDEV_ERROR_PrepareHeader


            The header for the audio device was being prepared.
          


### -field SNDDEV_ERROR_UnprepareHeader


            The header for the audio device was being unprepared.
          


### -field SNDDEV_ERROR_Reset


            The audio device attempted to reset.
          


### -field SNDDEV_ERROR_Restart


            The audio device attempted to restart.
          


### -field SNDDEV_ERROR_GetPosition


            The current and stop position settings were being retrieved.
          


### -field SNDDEV_ERROR_Write


            The audio device was being written to.
          


### -field SNDDEV_ERROR_Pause


            The audio device attempted to pause.
          


### -field SNDDEV_ERROR_Stop


            The audio device attempted to stop.
          


### -field SNDDEV_ERROR_Start


            The audio device attempted to start.
          


### -field SNDDEV_ERROR_AddBuffer


            A buffer was being added to the audio device.
          


### -field SNDDEV_ERROR_Query


            The audio device was being queried.
          


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>
 

 

