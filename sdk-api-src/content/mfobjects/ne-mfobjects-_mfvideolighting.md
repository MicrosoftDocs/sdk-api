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

# _MFVideoLighting enumeration


## -description



Describes the optimal lighting for viewing a particular set of video content.




## -enum-fields




### -field MFVideoLighting_Unknown

The optimal lighting is unknown.


### -field MFVideoLighting_bright

Bright lighting; for example, outdoors.


### -field MFVideoLighting_office

Medium brightness; for example, normal office lighting.


### -field MFVideoLighting_dim

Dim; for example, a living room with a television and additional low lighting.


### -field MFVideoLighting_dark

Dark; for example, a movie theater.


### -field MFVideoLighting_Last

Reserved.


### -field MFVideoLighting_ForceDWORD

Reserved. This member forces the enumeration type to compile as a <b>DWORD</b> value.


## -remarks



This enumeration is used with the <a href="https://msdn.microsoft.com/697590e3-898e-4ac9-8390-7b0994b6e571">MF_MT_VIDEO_LIGHTING</a> attribute.




## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/b8cfe0d1-013d-4706-bb76-6d426836ab6a">Video Media Types</a>
 

 

