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




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI Interface</a>
 

 

