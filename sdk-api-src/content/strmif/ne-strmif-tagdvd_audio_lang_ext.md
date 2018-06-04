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

# tagDVD_AUDIO_LANG_EXT enumeration


## -description



Defines flags that indicate whether an audio stream contains audio language extensions.




## -enum-fields




### -field DVD_AUD_EXT_NotSpecified


            The DVD doesn't specify an audio language extension for this audio stream.
          


### -field DVD_AUD_EXT_Captions


            The audio stream contains captions.
          


### -field DVD_AUD_EXT_VisuallyImpaired


            The audio stream contains content for people with low vision.
          


### -field DVD_AUD_EXT_DirectorComments1


            The audio stream contains "director comments 1."
          


### -field DVD_AUD_EXT_DirectorComments2


            The audio stream contains "director comments 2."
          


## -remarks



This enumeration is used in the <a href="https://msdn.microsoft.com/80291efa-f3eb-47f0-94e0-dcde583ff35c">IDvdInfo2::GetAudioAttributes</a> and <a href="https://msdn.microsoft.com/89f93521-9df7-4162-bb66-2210cceebc75">IDvdInfo2::GetDefaultAudioLanguage</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2</a>
 

 

